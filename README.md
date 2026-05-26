# Defensive UI Data Recovery Wizard (CLI-to-GUI wrapper)

A multi-step browser wizard interface designed to abstract raw command-line tools into safe interaction paths. This repository demonstrates defensive frontend engineering architectures that completely isolate user configurations, preventing catastrophic data corruption loops.

## The Engineering Problem

Deep block-level storage extraction utilities (such as `PhotoRec` or `ddrescue`) feature exceptionally powerful partition scanning logic but lack human system constraints. During hardware failures, users are usually operating under elevated stress. 

Forcing a frantic user to manually enter absolute console device arguments frequently leads to permanent data destruction. If an operator mistakenly mounts the destination target directly to the failing source partition, the extraction script immediately begins over-writing the very blocks it is attempting to scan.

## Defensive Design Strategy

This interface acts as an un-breakable protective filter around the underlying recovery engine:

* **Progressive Disclosure Sequencing:** Process complexity is divided cleanly into isolated, non-overlapping logical layout gates. Users are restricted to answering one configuration variable at a time, keeping cognitive strain down.
* **Client-Side Form Intercept Validation:** A strict target validation layer scans values inside the path fields in real time. If the script detects path overlaps ($\text{Target Path} \cap \text{Source Volume} \neq \emptyset$), the application immediately enters an absolute lock state, disabling execution controls to prevent write-corruption loops.
* **Automated Flag Interpolation:** Technical configurations (such as header clusters and file signature hex arrays) are toggled through semantic visual checkbox matrices. These selections are then automatically parsed to generate clean command strings in the background.

## Verification & Execution

Because this project adheres to native system specifications, it runs out of the box with zero runtime framework bloat or asset bundling requirements.

1. Clone the repository locally:
   ```bash
   git clone [https://github.com/cleo-coder/cli-to-gui-recovery-wizard.git](https://github.com/cleo-coder/cli-to-gui-recovery-wizard.git)