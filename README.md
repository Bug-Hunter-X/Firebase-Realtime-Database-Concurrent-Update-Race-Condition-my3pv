# Firebase Realtime Database Concurrent Update Race Condition

This repository demonstrates a subtle race condition in Firebase's Realtime Database when performing concurrent updates based on the current value of a data node.  The problem is particularly evident when attempting to increment a counter from multiple clients simultaneously.

The `bug.js` file contains the problematic code that shows the race condition. The `bugSolution.js` provides the corrected implementation using transactions to ensure atomicity.

## Setup

1.  Ensure you have Node.js and npm installed.
2.  Install the Firebase Admin SDK: `npm install firebase-admin`
3.  Create a Firebase project and configure the `firebase-admin.json` file.
4.  Run `node bug.js` and `node bugSolution.js` to observe the behavior.