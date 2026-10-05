---

# TeamCode Module

Welcome!

This module, **TeamCode**, is the place where you will write/paste the code for your team's robot controller app. This module is currently empty (a clean slate), but the process for adding OpModes is straightforward.

---

# GitHub Workflow (FTC Team)

Our GitHub workflow is as follows:

## 1. Write robot code

You commit normally:

```bash
git add .
git commit -m "robot code update"
git push origin main
```

This pushes to **your GitHub repo**, not the FTC SDK repo.

---

## 2. When the SDK updates

You pull from **upstream**, not origin:

```bash
git pull upstream main
```

This brings in **only SDK changes**.  
Your `TeamCode/` stays untouched.

If there are conflicts (only if you modified SDK files), Git will ask you to resolve them manually.

---

## 3. Keep your fork updated

If you want your GitHub fork to stay synced with upstream:

```bash
git push origin main
```

This updates your fork with the new SDK + your robot code.

---

# Creating Your Own OpModes

The easiest way to create your own OpMode is to copy a Sample OpMode and make it your own.

Sample OpModes exist in the **FtcRobotController** module.  
To locate these samples, find the FtcRobotController module in the *Project/Android* tab.

Expand the following tree elements:

```
FtcRobotController/java/org.firstinspires.ftc.robotcontroller/external/samples
```

---

## Naming of Samples

To better understand how the samples are organized, review the naming conventions described in `sample_conventions.md`.

Summary of prefixes:

- **Basic** — Minimal skeleton OpModes showing structure.
- **Sensor** — Demonstrates how to use a specific sensor.
- **Robot** — Assumes a simple two‑motor differential drive base.
- **Concept** — Demonstrates a specific function or concept.

Additional naming rules:

- Sensor: `Sensor - Company - Type`
- Robot: `Robot - Mode - Action - OpModetype`
- Concept: `Concept - Topic - OpModetype`

---

# Copying Samples into TeamCode

To use a sample as the basis for your robot:

1. Locate the desired sample class in the Project/Android tree.
2. Right‑click the sample class → **Copy**.
3. Expand the `TeamCode/java` folder.
4. Right‑click `org.firstinspires.ftc.teamcode` → **Paste**.
5. Choose a meaningful class name (start with a capital letter).

---

# Preparing Your OpMode

Each OpMode sample begins with:

```java
@TeleOp(name="Template: Linear OpMode", group="Linear Opmode")
@Disabled
```

- Change the `name="..."` to what you want displayed on the Driver Station.
- Optionally adjust the `group="..."`.
- Remove or comment out `@Disabled` to make the OpMode visible.

---