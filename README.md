# My CS Portfolio Project: Cross-Platform Design for The Gaming Room

## Project Summary & Client Expectations
This project was specifically created for my **Operating Platforms** course. The goal of this assignment was to work through a comprehensive software design document for a client studio called The Gaming Room. I was tasked with mapping out how to take their mobile, Android-only game, *Draw It or Lose It*—which is a round-based multiplayer game inspired by the 1980s TV show *Win, Lose or Draw*—and scale it up into a modern, web-based system. The software design needed to handle real-time sync across different operating systems, enforce absolute username uniqueness across a live network, and smoothly process 1.6 GBs of graphical game assets without crashing the central server.

## My Highlights in the Documentation Process
What stands out most in my design document is the Domain Model breakdown and the structured OS Evaluation Matrix. I managed to clearly map out how abstract Object-Oriented Programming (OOP) concepts translate into direct code architecture. For example, my UML diagram visually isolates how child classes like `Game`, `Team`, and `Player` inherit identity structures directly from a single parent `Entity` base class, while keeping core fields locked down from external tampering via strict private Encapsulation.

## Why the Design Stage Was Critical for Coding
Putting together this architectural framework before writing code saved me a massive amount of troubleshooting time later on. Because I had already established concrete system limitations on paper—like giving the central Java server ultimate authority over game loops and setting up the precise 15-second timer fallback for stealing points—I didn't have to guess or improvise while writing the backend logic. It allowed me to focus 100% on writing clean code because the blueprint was already set in stone.

## What I Would Change or Revise
Looking back at my work, the main section I would want to refine is the Recommendations area regarding memory efficiency and hardware storage. Even though my document points out great optimization paths like using Object Pooling and tiered background data pre-loading to manage that 1.6 GB asset bottleneck, it lacks concrete configuration details. If I were to write a revision, I would include actual Java code snippets and deployment setups to give the engineering team a literal instruction manual for production.

## Translating User Demands Into Technical Reality
To protect the player experience, I focused the design on cross-platform visual consistency and input parity, ensuring that UI elements never overlap on small screens and that buttons respond at identical speeds everywhere. Keeping the end-user in mind is vital because a system can be technically perfect, but it fails if it's frustrating to use. For this game, it meant engineering a web layer that lets a mobile user accurately sketch a puzzle with their fingers on a small touch screen while a desktop user on an operating system running Chrome or Firefox has the exact same snappy experience.

## System Architecture Strategy and Next Steps
My overall design approach relied heavily on a structured Client-Server Architecture controlled by an object-oriented backend. The core server runtime uses a memory-conscious Singleton pattern for the `GameService` engine and abstracts complex entity generation via backend Factory-style methods (`addTeam` and `addPlayer`). Going forward, I will definitely keep using container tools like Docker and automation tools like Maven to build clean environments, but I plan to introduce interactive wireframing loops even earlier in my planning phase to map real-time validation checks out even faster.
