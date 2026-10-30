# Rusterm-Audio-VL
A Terminal User Interface (TUI) audio visualizer written in Rust.

Rusterm-Audio-VL processes incoming audio streams—either from a local file or live microphone input—and extracts frequency and waveform data (bass, mids, highs, treble) to generate dynamic, real-time visualizations directly in your terminal.

Features
Core Visualizations
Classic Bar Chart: A standard frequency equalizer rendered in the terminal. Frequency data is divided into blocks, mapping amplitude to the height of the columns.

Rainfall / Tetris Mode: A grid-based emergent visualizer. Blocks spawn at the top of the screen with colors and quantities mapped to frequency intensities. Blocks fall, stack at the bottom, and clear either on a timer or when a full line is completed.

Audio Input Support
File Playback: Provide a file path to an audio file.

Live Microphone Input: Reacts dynamically to your environment or system audio.

Tech Stack & Dependencies
This project leverages the Rust ecosystem for audio processing and terminal rendering:

Ratatui / Crossterm: For handling terminal windowing, app state, and colored character drawing.

Rodio / cpal: For audio file playback and cross-platform audio I/O.

spectrum-analyzer: For Fast Fourier Transforms (FFT) to convert audio waveforms into usable frequency spectrum data.

Roadmap & Stretch Goals
While the core focus is on the visualizer, the eventual goal is to expand the project into a fully-featured terminal audio player with dedicated TUI windows.

[ ] Playback Controls: Runtime keybindings for Play, Pause, and Stop.

[ ] Scrubbing: Fast forward and reverse track seeking (5-second increments).

[ ] Track Timeline: A visual progress bar tied to the track's percentage of completion.

[ ] TUI File Browser: A dedicated window to navigate directories, view audio files, and select tracks at runtime.

[ ] Metadata Extraction: Read and display ID3 tags/metadata (Artist, Title, Album) instead of raw filenames.

[ ] Terminal Album Art: Extract and render music/album covers directly in the terminal using block characters or sixel graphics.

About
Author: Gustavo Carrillo Castro (gustav5@pdx.edu)

Course: CS523: Programming Rust

This project is built as a course project exploring Rust's concurrency, app state management, and real-time data processing.
