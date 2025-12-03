# 🧠 Neural Network

Neural Network is a lightweight C# implementation of a fully-custom deep learning framework, built from scratch without external ML libraries.
It includes vector/matrix math utilities, configurable network layers, training utilities, MNIST data loading, and a minimal UI canvas for visualizing predictions.

![alt text](Neural-Network/Resources/Media/Screenshot.png)

# Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Architecture](#architecture)
* [Setup Instructions](#setup-instructions)
* [Testing Guide](#testing-guide)
* [Modifying the Codebase](#modifying-the-codebase)
* [License](#license)
* [Contact Information](#contact-information)

# Overview

This project implements a neural network framework in pure C#.
It includes mathematical primitives, layer definitions, feedforward/backprop logic, data parsers, and a lightweight UI to visualize training and inference—ideal for learning and experimenting with deep learning fundamentals.

It’s clean, modular, and easy to extend with new layer types or cost functions.

# Features

* Fully custom matrix & vector math (no external dependencies)
* Configurable feedforward neural networks
* Backpropagation & gradient descent training
* MNIST dataset loader (`mnist.csv`)
* Model saving & loading (`Resources/Models/mnist.txt`)
* Simple drawn UI canvas for visualizing predictions
* Modular architecture—easy to add layers, activations, or utilities

# Architecture

| Component            | Description                                                        |
| -------------------- | ------------------------------------------------------------------ |
| `Matrix` / `Vector`  | Custom math classes optimized for neural-network operations        |
| `Layer`              | Represents a single NN layer with weights, biases, and activations |
| `Network`            | Manages layer stack, training, inference, and propagation logic    |
| `CostParser`         | Parses and applies cost/loss functions                             |
| `DataParser`         | Loads and preprocesses training data (MNIST, CSV input, etc.)      |
| `Canvas`             | Draws digits/input data for UI testing                             |
| `ScoreBoard`         | Displays prediction results and training metrics                   |

# Setup Instructions

1. **Install .NET SDK**

   - Requires **.NET 6.0 or higher**
   - Download here:
     [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
   - Verify installation:
     ```bash
     dotnet --version
     ```

2. **Clone the Repository**
   ```bash
   git clone https://github.com/AndriaBeridze/Neural-Network.git
   cd Neural-Network
   ```

3. **Run the Application**
   ```bash
   dotnet run
   ```

# Testing Guide

* After launching, a UI window will appear containing a drawing canvas.
* Draw a digit using your mouse.
* The neural network will process your drawing and output the predicted digit in the scoreboard area.
* If using MNIST data, predictions will update in real time as you draw.

# Modifying the Codebase

* To change the training logic or network architecture, edit: `Scripts/Network/Network.cs`, `Scripts/Network/Layer.cs`
* For matrix/vector operations (e.g., numerical optimization), modify: `Scripts/Math/Matrix.cs`, `Scripts/Math/Vector.cs`
* To customize MNIST or CSV parsing, see: `Scripts/Network/Helpers/DataParser.cs`
* To change UI visuals or add new controls, modify: `Scripts/App/UI/`
* For themes, colors, or default application settings: `Scripts/App/Utility/Theme.cs`, `Scripts/App/Utility/Settings.cs`

# License

This project is open source and licensed under the **GNU Affero General Public License (AGPL)**.

You are free to use, modify, and distribute this software for personal or commercial purposes, provided that any distributed versions also comply with the AGPL terms, including making source code available.

**No warranty is provided. Use at your own risk.**

# Contact Information

| Name           | Phone Number      | Email                                             | LinkedIn                                                                    |
| -------------- | ----------------- | ------------------------------------------------- | --------------------------------------------------------------------------- |
| Andria Beridze | +1 (267) 632-6754 | [andria24b@gmail.com](mailto:andria24b@gmail.com) | [linkedin.com/in/andriaberidze](https://www.linkedin.com/in/andriaberidze/) |
