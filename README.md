## FRC 2026 10367 GENERAL DOCS

## 📦 Subsystems

- **Drive**  
  - Supports TalonFX hardware and simulation.  
  - Gyro integration via NavX or simulated gyro.  

- **Superstructure**  
  - Handles intake, launching, and ejecting mechanisms.  
  - Hardware (TalonFX) and simulation implementations available.  

---

## 🎮 Controls (Xbox Controller)

| Control                | Action |
|-------------------------|--------|
| **Left Stick (Y-axis)** | Forward/Backward drive (arcade drive, scaled to 80%) |
| **Right Stick (X-axis)**| Turning (arcade drive, scaled to 80%) |
| **A Button**            | Eject game piece |
| **B Button**            | Intake + Launch combined (`intklnch`) |
| **Left Bumper**         | Intake game piece |
| **Right Bumper**        | Launch game piece |

---

## 🤖 Autonomous Modes

Autonomous routines are selectable via the **LoggedDashboardChooser**:

- **PathPlanner Auto Chooser** – Runs prebuilt autonomous paths.  
- **SysId Routines** – For drivetrain characterization:  
  - Drive Simple Feedforward Characterization  
  - Quasistatic Forward / Reverse  
  - Dynamic Forward / Reverse  

Additionally, a custom **Launch** command is registered for autonomous use.

---

## 🛠️ Development Modes

The robot supports three modes via `Constants.currentMode`:

- **REAL** – Uses hardware IO (TalonFX, NavX).  
- **SIM** – Uses physics simulation IO.  
- **REPLAY** – Disables IO for log replay.  

---

## 📖 Notes

- **Command-based structure**: Subsystems define hardware, commands define actions, and `RobotContainer` wires everything together.  
- **Button bindings**: Configured in `configureButtonBindings()`.  
- **Autonomous selection**: Accessible through Shuffleboard/SmartDashboard via `autoChooser`.  

---

This README provides a quick reference for controls, subsystems, and autonomous routines so drivers and programmers can easily understand the robot’s functionality.
