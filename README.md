# Motoko PhoneBook & Messaging System

This project is a simple **phone book** and **messaging system** written in the **Motoko programming language**, designed for the **Internet Computer (IC)** platform. It demonstrates how to use `HashMap` to store and query data efficiently.

---

## Features

- **Phone Book Management**:
  - Add new entries to the phone book.
  - Retrieve contact information by name.

- **Messaging System**:
  - Send and store messages from a sender's phone.
  - Query message history based on sender's phone number.

---

## Installation and Usage

### Prerequisites

1. Install the [DFINITY SDK](https://internetcomputer.org/docs/current/developer-docs/quickstart/).
2. Ensure you have a stable environment to deploy Internet Computer actors.

### Steps to Deploy

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/motoko-phonebook.git
   cd motoko-phonebook

2. Deploy the actor on the Internet Computer:
   ```bash
   dfx start --background
   dfx deploy

3. Interact with the deployed actor using the Motoko REPL or HTTP API.

## Actor API

### Phone Book Methods

- `insert(name: Name, entry: Entry): async ()`
  - Adds a new entry to the phone book.
  - Example:
  ```motoko
  insert("Alice", {desc = "Friend"; phone = "12345"});
  
- `getPhone(name: Name): async ?Entry`
  - Retrieves an entry by name.
  - Example:
  ```motoko
  getPhone("Alice"); // Returns: {desc = "Friend"; phone = "12345"}


