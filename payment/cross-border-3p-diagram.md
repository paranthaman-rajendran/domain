sequenceDiagram
    participant Sender Bank
    participant Sender
    participant Third-Party Bank
    participant Receiver Bank
    participant Receiver

    Sender->>Sender Bank: Initiates Payment Request
    Sender Bank->>Third-Party Bank: Sends Payment Instruction
    Third-Party Bank->>Third-Party Bank: Performs Compliance Checks
    Third-Party Bank->>Third-Party Bank: Converts Currency (if needed)
    Third-Party Bank->>Receiver Bank: Forwards Payment Instruction
    Receiver Bank->>Receiver Bank: Posts Payment to Account
    Receiver Bank->>Receiver: Notifies Payment Received
    Receiver Bank-->>Third-Party Bank: Sends Payment Confirmation
    Third-Party Bank-->>Sender Bank: Sends Payment Confirmation
    Sender Bank-->>Sender: Notifies Payment Processed
