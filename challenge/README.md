# LAYR 25/26: The Challenge

#### Content:
1. Storyline: The "Guardian" Assignment
2. Tasks
    2.1 Build a microchip
    2.2 Battle of the teams
3. Timeline and Milestones
4. Deliverables
5. Judging criteria

## 1. Storyline: The "Guardian" Assignment

You and your entire team were recently hired to design the core of a next-generation security system guarding a classified research vault. The vault has a physical door lock that is supposed to be opened by traditional keycards. Your task is to design this digital system. Because you have leftover budget for manufacturing your custom chip, you start “Project Guardian”, which is a great opportunity to deploy a custom chip.

This “Guardian” chip must be able to securely perform some form of authentication protocol (more details later) with the keycard and, if the card succeeds and returns an authorized ID, activate the door's locking mechanism. Your chip will interface with the outside world through two critical communication channels:

* **Keycard reader:** This is your primary input. The chip will need to communicate with a provided contactless ISO/IEC 14443-A card reader via a Serial Peripheral Interface (SPI). Depending on the chosen Security-by-Design (more details later), different protocol messages need to be exchanged with the smart card.
* **Switch interface:** This is your primary output. Once the chip has verified the access privileges of the card holder, it must set the corresponding output pin to a high logic level. This signal will be the electronic "key" that unlocks the door.

Additionally, there is an **SPI-EEPROM** located on the development board, which will be used as non-volatile storage to hold a shared key between the lock and the keycard for authentication purposes (only applicable on higher security levels) and the list of allowed card IDs that should have access to the given door.

Your design should consist of a digital logic circuit described in a Hardware Description Language (HDL). The ultimate goal is to create a small, fast, and secure chip.

**Competition!** Today you found out that not only your team will work for this chip, but that many more teams across your entire enterprise were tasked to complete this crucial project. You are all competing in a challenge!

All teams share the same design environment, templates and test benches to start your work on. As the security level is not fixed yet, your team can freely choose from four different security levels to target.

Note: For more information on judging criteria, we refer to our separate competition guidelines.

## 2. Tasks

#### 2.1 Build a microchip

#### 2.2 Battle of the teams

## 3. Timeline and Milestones

## 4. Deliverables

## 5. Judging criteria
 