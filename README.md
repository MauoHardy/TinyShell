# Tiny Shell (tsh)

## Overview
The Tiny Shell (tsh) is a custom-built UNIX shell implemented in C, providing essential features such as process control, signal handling, and support for pipelines. This project was developed as part of a Systems Programming Course and includes additional capabilities like audio processing and a multiplayer gaming environment within the shell.

## License:
The project repsitory with the actual code is not public according to the Academic Conduct of UofT, for access to the private repo email me at hj.shah@mail.utoronto.ca

## Features

### 1. Core Shell Functionality
- **Process Control:**
  - Foreground and background job management.
  - Job state transitions (e.g., `CTRL-Z` to stop jobs, `fg` to resume jobs in the foreground).
- **Signal Handling:**
  - Proper handling of `SIGINT` (CTRL-C), `SIGTSTP` (CTRL-Z), and `SIGCHLD` signals.
  - Graceful termination of the shell using `SIGQUIT`.
- **Command Execution:**
  - Handles built-in commands (`quit`, `jobs`, `bg`, `fg`).
  - Executes external commands and scripts.
  - Supports input/output redirection (`<`, `>`).
  - Implements pipelines (`|`) for chaining commands.

### 2. Enhanced Audio Processing
- **WAV File Echo Effect:**
  - Users can add or remove an echo effect in `.WAV` audio files directly from the shell.
  - This feature demonstrates practical signal processing capabilities within the shell environment.

### 3. Interactive Multiplayer Game Environment
- **Socket Programming Integration:**
  - Enables text-based multiplayer gameplay within the shell.
  - Implements automatic opponent queuing to minimize idle time.
  - Provides an interactive and engaging experience within the command-line interface.

## Installation
1. Clone the repository: (For access email me)
2. Navigate to the project directory:
   ```bash
   cd tiny-shell
   ```
3. Compile the shell:
   ```bash
   gcc -o tsh tsh.c
   ```

## Usage
Run the shell with:
```bash
tsh
```

### Available Commands
- `jobs` – List currently running jobs.
- `bg <job>` – Resume a job in the background.
- `fg <job>` – Bring a background job to the foreground.
- `quit` – Exit the shell.
- `<command> > <output_file>` – Redirect output to a file.
- `<command> < <input_file>` – Redirect input from a file.
- `<command1> | <command2>` – Use pipelines to combine commands.
- `audio_echo add/remove <file.wav>` – Add or remove echo effect in WAV files.
- `playgame` – Start the multiplayer game.

## Implementation Details
- **Job Control:** Implemented using process IDs and job IDs.
- **Signal Handling:** Utilizing `sigaction` for robust signal management.
- **I/O Redirection:** Handled with `dup2` system calls.
- **Multiplayer Game:** Built using TCP sockets for network communication.

## Future Enhancements
- Support for additional built-in commands.
- Improved job management features.
- More audio processing effects.
- Enhanced game features with better matchmaking.

## Contributors
- Hardik Shah
- Harsh Mehta
- Andy Tran

