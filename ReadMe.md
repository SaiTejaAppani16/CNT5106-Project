
# 📡 Peer-to-Peer File Sharing System – Group 16

## 🔍 Project Summary
This project presents a decentralized peer-to-peer (P2P) file sharing application, modeled after BitTorrent.
It enables multiple peers to exchange file segments through TCP sockets, eliminating the need for a central server.
Core features include intelligent choking/unchoking mechanisms, peer prioritization, and file chunking for faster, parallel downloads.

## 🎯 Key Features
- Decentralized communication between peers using TCP sockets.
- Dynamic choking and unchoking to prioritize peers based on download contribution.
- File is split into segments for parallel downloading from multiple peers.
- Logging of system events for monitoring and debugging purposes.

## 🛠️ Setup Instructions

### 🔧 Compilation
To compile all Java files, run:
```
javac *.java
```

### 🚀 Running the Application
Start each peer process with its peer ID:
```
java Peer 1001
java Peer 1002
java Peer 1003
```

### 📽️ Demo Video
[Watch the demo](https://uflorida-my.sharepoint.com/personal/saipande_ufl_edu/_layouts/15/stream.aspx?id=%2Fpersonal%2Fsaipande%5Fufl%5Fedu%2FDocuments%2FComputer%20Network%2Emp4)

## ⚙️ Configuration Files

### `Common.cfg`
```
NumberOfPreferredNeighbors 3
UnchokingInterval 5
OptimisticUnchokingInterval 10
FileName tree.jpg
FileSize 24301568
PieceSize 1638400
```

### `PeerInfo.cfg`
```
1001 localhost 6003 1
1002 localhost 6004 0
1003 localhost 6005 0
```

## 🔧 Core Components
- `refreshPreferredPeers()` – Dynamically selects preferred peers based on download performance.
- `chooseOptimisticPeer()` – Randomly unchokes one peer to ensure fairness in sharing.
- `mergeChunks()` – Reconstructs the full file from received segments once all chunks are collected.

## 💡 Conclusion
This system successfully simulates the functionality of a distributed file sharing network.
It demonstrates practical applications of fairness, parallelism, and network programming through peer prioritization and chunk-based file transfers.

## 👥 Team Members – Group 16
- Sriram Thota – UFID: [Add Here]
- Nabeel Ahmed Mohammed – UFID: 33179038
- Sai Teja Appani – UFID: 53834314
