BinNode-Tunnel is a high-performance, cross-platform intranet penetration and mesh networking solution built with Golang. Designed for resilience and speed, it utilizes the KCP protocol (Reliable UDP) to ensure stable transmission even over high-latency networks.

The core strength of BinNode-Tunnel lies in its intelligent hybrid traffic routing. The system prioritizes direct P2P connections (NAT hole punching) between nodes to maximize throughput and minimize latency. If a direct connection cannot be established, it seamlessly fails over to a Master server relay, ensuring 100% connectivity availability. All internal communication is serialized using Protocol Buffers (Protobuf), guaranteeing high efficiency, type safety, and future extensibility.

Security and ease of use are paramount. Nodes are isolated via strict NetID and password authentication, preventing unauthorized access across different network groups. The software features a unique "Zero-Config" deployment capability, allowing new nodes to fetch initialization templates via DNS TXT records automatically.

BinNode-Tunnel provides a native user experience across platforms: a lightweight Win32 System Tray GUI for Windows and a robust, tcell-based TUI for Linux (supporting amd64 and ARM architectures). It automatically manages local port mapping and service discovery, making remote access to SSH, web servers, or RDP seamless.
Key Features List (Optional for README):

    Hybrid Connectivity: Automatic P2P Direct Connect with Relay Fallback.
    Protocol: Fast KCP transport + Smux multiplexing + Protobuf serialization.
    Cross-Platform: Native Windows GUI & Linux Terminal UI (TUI).
    Security: Network isolation via NetID/Password and UUID identity.
    Persistence: Automatic port mapping restoration and configuration saving.
