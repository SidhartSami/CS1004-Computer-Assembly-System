<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/SidhartSami/Computer-Assembly-System">
    <img src="images/logo.png" alt="Computer Assembly Logo" width="80" height="80">
  </a>

  <h3 align="center">Computer Assembly System</h3>

  <p align="center">
    A comprehensive Object-Oriented Programming project demonstrating class hierarchy and component composition for building custom PC and Mac systems.
    <br />
    <a href="https://github.com/SidhartSami/Computer-Assembly-System"><strong>Explore the Repository »</strong></a>
    <br />
    <br />
    <a href="https://github.com/SidhartSami/Computer-Assembly-System">View Code</a>
    ·
    <a href="https://github.com/SidhartSami/Computer-Assembly-System/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    ·
    <a href="https://github.com/SidhartSami/Computer-Assembly-System/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#features">Features</a>
    </li>
    <li>
      <a href="#class-hierarchy">Class Hierarchy</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#compilation">Compilation</a></li>
      </ul>
    </li>
    <li><a href="#project-structure">Project Structure</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#key-components">Key Components</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

Computer Assembly System is an Object-Oriented Programming project developed as part of the CS-1004 course at FAST NUCES (National University of Computer & Emerging Sciences), Islamabad during Spring 2024. This project demonstrates advanced OOP concepts including inheritance, composition, aggregation, and polymorphism through a real-world computer assembly scenario.

The system allows users to design and build custom computers (PC or Mac) by selecting various components such as processors, memory, storage devices, and peripherals. It validates component compatibility based on the selected computer type and calculates the total system price.

Here's why this project is significant:

* Demonstrates mastery of class hierarchies and object-oriented design patterns
* Implements real-world component relationships using composition and aggregation
* Provides comprehensive error handling and input validation
* Showcases proper resource management and memory allocation
* Includes detailed UML diagrams illustrating class relationships
* Follows industry-standard naming conventions and coding practices

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

This project is built using:

* [![C++][Cpp.com]][Cpp-url]
* Object-Oriented Programming (OOP) principles
* Standard C++ libraries (without external dependencies)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- FEATURES -->
## Features

* **Multiple Computer Types** - Support for PC and Mac systems with architecture-specific components
* **CPU Architecture Support** - Intel/AMD (x86) and AppleSilicon (ARM64) processors
* **Memory Type Handling** - DDR4/5 for PC systems and LPDDR4/5 for Mac systems
* **GPU Integration** - Discrete GPUs (Nvidia, AMD) for PCs and integrated AppleGPU for Macs
* **Component Composition** - ALU and Control Unit composition within CPU
* **Motherboard Assembly** - Multiple port types and memory aggregation
* **Storage Options** - HDD, SSD, and NAS HDD support
* **Comprehensive Validation** - Input validation and component compatibility checking
* **Price Calculation** - Automatic total system price computation
* **Dynamic Object Management** - Proper memory allocation and deallocation
* **Detailed Display** - Complete system specifications output

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CLASS HIERARCHY -->
## Class Hierarchy

### Core CPU Components
* **ALU** - Arithmetic Logic Unit with adders, subtractors, and registers
* **ControlUnit** - Clock management and control logic
* **CPU** - Composition of ALU and ControlUnit

### CPU Types (Inheritance from CPU)
* **IntelAMD_CPU** - x86 architecture processor
* **AppleSilicon_CPU** - ARM64 architecture with integrated GPU

### Memory Components
* **MainMemory** - Primary memory interface
* **PhysicalMemory** - Base class for physical memory types
  * **DDR4_5** - For Intel/AMD systems
  * **LPDDR4_5** - For AppleSilicon systems

### System Components
* **Port** - I/O connectivity (USB, HDMI, VGA, etc.)
* **MotherBoard** - Composition of ports and aggregation of MainMemory
* **GraphicsCard** - Discrete GPU (Nvidia, AMD) or integrated AppleGPU
* **StorageDevice** - Storage media (HDD, SSD, NAS HDD)
* **NetworkCard** - Network connectivity
* **PowerSupply** - System power requirements
* **Battery** - Portable device power source
* **Case** - System housing with form factor

### High-Level Assembly
* **Computer** - Aggregation of CPU, MotherBoard, and PhysicalMemory
* **ComputerAssembly** - Complete system with all components and pricing
  * **PC** - Personal Computer (inherits from ComputerAssembly)
  * **Mac** - Apple Macintosh (inherits from ComputerAssembly)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

Follow these instructions to compile and run the Computer Assembly System on your local machine.

### Prerequisites

You will need the following to compile and run this project:

* A C++ compiler (GCC, Clang, or MSVC)
  ```sh
  # Check if you have g++ installed
  g++ --version
  ```
* A text editor or IDE (Visual Studio Code, Code::Blocks, etc.)
* Command line terminal/console access

### Installation

1. Clone the repository
   ```sh
   git clone https://github.com/SidhartSami/Computer-Assembly-System.git
   ```

2. Navigate to the project directory
   ```sh
   cd Computer-Assembly-System
   ```

3. Verify the file structure
   ```sh
   ls -la  # On macOS/Linux
   dir     # On Windows
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Compilation

Compile the project using g++ compiler:

**For Linux/macOS:**
```sh
g++ -std=c++11 -o ComputerAssembly *.cpp
```

**For Windows (MinGW):**
```sh
g++ -std=c++11 -o ComputerAssembly.exe *.cpp
```

**Using a Makefile (if provided):**
```sh
make
```

### Running the Program

After successful compilation:

**For Linux/macOS:**
```sh
./ComputerAssembly
```

**For Windows:**
```sh
ComputerAssembly.exe
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PROJECT STRUCTURE -->
## Project Structure

```
Computer-Assembly-System/
├── Code/                        # C++ source files
│   ├── ALU.h                    # ALU class header
│   ├── ALU.cpp                  # ALU class implementation
│   ├── ControlUnit.h            # ControlUnit class header
│   ├── ControlUnit.cpp          # ControlUnit implementation
│   ├── CPU.h                    # CPU base class header
│   ├── CPU.cpp                  # CPU implementation
│   ├── IntelAMD_CPU.h           # x86 architecture CPU header
│   ├── IntelAMD_CPU.cpp         # x86 CPU implementation
│   ├── AppleSilicon_CPU.h       # ARM64 architecture CPU header
│   ├── AppleSilicon_CPU.cpp     # ARM64 CPU implementation
│   ├── MainMemory.h             # MainMemory class header
│   ├── MainMemory.cpp           # MainMemory implementation
│   ├── PhysicalMemory.h         # PhysicalMemory base class header
│   ├── PhysicalMemory.cpp       # PhysicalMemory implementation
│   ├── DDR4_5.h                 # DDR memory class header
│   ├── DDR4_5.cpp               # DDR implementation
│   ├── LPDDR4_5.h               # Low Power DDR header
│   ├── LPDDR4_5.cpp             # LPDDR implementation
│   ├── Port.h                   # Port class header
│   ├── Port.cpp                 # Port implementation
│   ├── MotherBoard.h            # MotherBoard class header
│   ├── MotherBoard.cpp          # MotherBoard implementation
│   ├── GraphicsCard.h           # GraphicsCard base class header
│   ├── GraphicsCard.cpp         # GraphicsCard implementation
│   ├── Nvidia_GPU.h             # Nvidia GPU header
│   ├── Nvidia_GPU.cpp           # Nvidia GPU implementation
│   ├── AMD_GPU.h                # AMD GPU header
│   ├── AMD_GPU.cpp              # AMD GPU implementation
│   ├── AppleGPU.h               # Apple GPU header
│   ├── AppleGPU.cpp             # Apple GPU implementation
│   ├── StorageDevice.h          # StorageDevice class header
│   ├── StorageDevice.cpp        # StorageDevice implementation
│   ├── HDD.h                    # HDD class header
│   ├── HDD.cpp                  # HDD implementation
│   ├── SSD.h                    # SSD class header
│   ├── SSD.cpp                  # SSD implementation
│   ├── NAS_HDD.h                # NAS HDD header
│   ├── NAS_HDD.cpp              # NAS HDD implementation
│   ├── NetworkCard.h            # NetworkCard class header
│   ├── NetworkCard.cpp          # NetworkCard implementation
│   ├── PowerSupply.h            # PowerSupply class header
│   ├── PowerSupply.cpp          # PowerSupply implementation
│   ├── Battery.h                # Battery class header
│   ├── Battery.cpp              # Battery implementation
│   ├── Case.h                   # Case class header
│   ├── Case.cpp                 # Case implementation
│   ├── Computer.h               # Computer class header
│   ├── Computer.cpp             # Computer implementation
│   ├── ComputerAssembly.h       # ComputerAssembly base class header
│   ├── ComputerAssembly.cpp     # ComputerAssembly implementation
│   ├── PC.h                     # PC class header
│   ├── PC.cpp                   # PC implementation
│   ├── Mac.h                    # Mac class header
│   ├── Mac.cpp                  # Mac implementation
│   └── main.cpp                 # Main program entry point
├── UML/
│   └── ComputerAssembly_UML.pdf # Detailed UML class diagram
├── Documentation/               # Additional documentation
├── README.md                    # Project documentation
└── LICENSE.txt                  # License information
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->
## Usage

### Running the Program

1. Launch the application
   ```sh
   ./ComputerAssembly
   ```

2. Select computer type (PC or Mac)
   ```
   Welcome to Computer Assembly System
   Select Computer Type:
   1. PC
   2. Mac
   Enter your choice: 1
   ```

3. Configure CPU specifications
   ```
   Enter CPU details:
   Number of Adders: 8
   Number of Subtractors: 8
   Number of Registers: 32
   Size of Registers: 64
   Clock Speed (GHz): 3.5
   ```

4. Select memory configuration
   ```
   Enter Memory Capacity (GB): 16
   Enter Memory Type: DDR5
   ```

5. Configure storage devices
   ```
   Add Storage Devices
   Storage Type (HDD/SSD): SSD
   Storage Capacity (GB): 512
   Storage Price ($): 80
   ```

6. Add additional components (GPU, Network Card, etc.)

7. View final specifications and total price
   ```
   ====== Computer Specifications ======
   CPU: Intel Core i7 (x86)
   Memory: 16GB DDR5
   GPU: RTX 3060
   Storage: 512GB SSD
   Network: Gigabit Ethernet
   
   Total Price: $1,299.99
   ```

### Error Handling

The system validates all inputs and provides helpful error messages:

```
Invalid input! Please enter a valid integer.
Incompatible component for selected system type.
Please restart and select appropriate components.
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- KEY COMPONENTS -->
## Key Components

### ALU (Arithmetic Logic Unit)
Manages computational operations with configurable adders, subtractors, and registers.

### Control Unit
Manages system clock and control signals with configurable clock frequency.

### CPU Variants
* **IntelAMD_CPU** - x86 architecture supporting DDR4/5 memory and discrete GPUs
* **AppleSilicon_CPU** - ARM64 architecture with integrated GPU and LPDDR4/5 support

### Memory Hierarchy
* **MainMemory** - Primary system memory interface
* **DDR4_5** - Standard DRAM for desktop systems
* **LPDDR4_5** - Low-power memory for mobile systems

### I/O Ports
Support for various connection types: USB, HDMI, DisplayPort, Ethernet, and VGA.

### Storage Options
* **HDD** - Traditional hard disk drives
* **SSD** - Solid-state drives for faster performance
* **NAS HDD** - Network-attached storage drives

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

This project was developed as an academic assignment for FAST NUCES CS-1004 Object Oriented Programming course (Spring 2024).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

**Sidhart Sami**

Email: [sidhart.sami@gmail.com](mailto:sidhart.sami@gmail.com)

GitHub: [@SidhartSami](https://github.com/SidhartSami)

Project Link: [https://github.com/SidhartSami/Computer-Assembly-System](https://github.com/SidhartSami/Computer-Assembly-System)

Course: CS-1004 Object Oriented Programming, FAST NUCES Islamabad, Spring 2024

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Special thanks to the following resources and institutions:

* [FAST NUCES](https://www.fast.edu.pk) - Educational institution and course provider
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template) - README structure and format
* Course Instructor and Teaching Assistants for guidance and support
* C++ Standard Library Documentation
* Object-Oriented Design Principles and Patterns
* All peer reviewers and contributors

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/SidhartSami/Computer-Assembly-System.svg?style=for-the-badge
[contributors-url]: https://github.com/SidhartSami/Computer-Assembly-System/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/SidhartSami/Computer-Assembly-System.svg?style=for-the-badge
[forks-url]: https://github.com/SidhartSami/Computer-Assembly-System/network/members
[stars-shield]: https://img.shields.io/github/stars/SidhartSami/Computer-Assembly-System.svg?style=for-the-badge
[stars-url]: https://github.com/SidhartSami/Computer-Assembly-System/stargazers
[issues-shield]: https://img.shields.io/github/issues/SidhartSami/Computer-Assembly-System.svg?style=for-the-badge
[issues-url]: https://github.com/SidhartSami/Computer-Assembly-System/issues
[license-shield]: https://img.shields.io/github/license/SidhartSami/Computer-Assembly-System.svg?style=for-the-badge
[license-url]: https://github.com/SidhartSami/Computer-Assembly-System/blob/main/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/i
