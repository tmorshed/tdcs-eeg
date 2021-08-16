# EEG-tDCS recording checklist

**Purpose**: This is to guide the setup for tDCS-EEG experiments at the KCNI EEG Lab. 

**Lab Location**: CAMH, 250 College St – Room 604

## Materials needed

- 1x [Soterix Medical mini-CT tDCS stimulator](https://soterixmedical.com/research/remote/mini-CT)
- 1x [Cortech Solutions 10-20 EEG Cap](https://cortechsolutions.com/product-category/eeg-ecg-emg-systems/eeg-ecg-emg-systems-activetwo/eeg-ecg-emg-systems-activetwo-head-caps/)
- 2x [Soterix Medical SNAPpad](https://soterixmedical.com/research/1x1/accessories/snappad) > 5x5cm size
- 2x Anode + Cathode tDCS cables. Either:
  - 1x [Soterix SNAPstrap](https://soterixmedical.com/research/1x1/accessories/snapstrap): Must detach the cable and snap electrode from the headband; or:
  - 2x [Soterix Medical mini-CT connecting cables](https://soterixmedical.com/research/1x1/accessories/1x1-Mini-CT-Connecting-Cables) + 2x Electrode snap connectors detached from a SNAPstrap.
- 64x EEG channel cables (sets A and B).
- 1x [Parker Inc. Signa gel tube](https://cortechsolutions.com/product/cs-gp-egsg12/)
- 1x Non-sterile curved tip plastic irrigation syringe e.g., [this option](https://www.canadawide.ca/Catalogue/Equipment/Categories/Monoject-Curved-Tip-Syringe/Item/Monoject-Curved-Tip-Syringe/839-205.3/1311).
  
## Steps

### a. Preparing the tDCS-EEG contraption

#### In the main room:
- Based on your desired tDCS montage, remove the respective electrodes mounts from the EEG caps, to make space for the tDCS sponges. 
  - Also, remove the 4 immediately adjacent electrodes to make space for the sponge.
    - List of all holes to be removed for the F3-F4 stimulation montage: F1-F3-F5-AF3-FC3, F2-F4-F6-AF4-FC4.
  - Make sure you store both the internal and external pieces in a safe place (e.g., in a small ziploc bag)
  - At the KCNI EEG lab, we currently use the F3-F4 montage.
- Put in the sponges in the pertinent locations.

#### At the Faraday cage, with the subject:
- Connect the snap cables to the SNAPpad square sponges.
- Connect the banana cables to the miniCT stimulator.
- Add gel to a syringe > Fill it up.
- Apply the gel to all remaining EEG electrode locations.
  - Add gel until it fills the mounting point on the node and is *just* overflowing.
- Connect the EEG electrodes on all available nodes and the extras based on the 10-20 system
  - Connect the CMS/DRL electrodes.
  - Connect the EX electrodes (extras) based on the SOP (OPS226: page 4).
- Connect the cables to the their sockets on the EEG amplifier box.

#### b. Connect the amplifier and check

- Turn on the amplifier via the button on the front of the box.
- Proceed to the "EEG Measurement Computer" monitor. On the ActiView software, navigate to the "Electrode Offset" tab.
- Make sure that all the recording electrodes have <20 offset.
  - Reminder: 10 electrodes at and around F3-F4 are removed, so they will all have astronomical offset levels.
  - To fix the electrodes' offset levels, remove them, add more gel, and put them back on.
  - If you see widespread high offset, it might be because of bad CMS/DRL signal. In those cases, you would want to re-do the CMS/DRL electrodes only.
  - After all levels are normalized, you can go forward with the rest of the exp.

#### c. Set up the tDCS codes:
- Turn on the miniCT device.
- Go to the "administration" option.
- Enter the password (*chmod*)
- Choose "generate new codes"
- Choose a subject number
- Choose 2.0mA
- Choose sham on/off condition.
  - Sham *on* is sham, the control arm. Sham *off* is actual tDCS, the active arm.
- Choose the quantity (number) of codes. Remember that for doing the trial 3 times you need 3 separate codes, as they are single-use.
- Jot down the codes.

### d. Get ready to start the experiment

- Explain the procedure to the participant.
  > Rest - stim - rest, 10m each.

  > Questions?

  #### d.0. ***only for stim trials***, skip to d.1 for normal trials.: 
  - Describe tDCS procedure for the subject.
  - Input the stimulation code but do not press run.
  - Tell the subject to wait for your verbal cue to start the experiment.
  - After finishing d.1 and d.2:
    - Quickly get back to the room, and start tDCS.
    - Tell the subject to "start the experiment now".
    - Get out of the Faraday cage.


  ### Back at the main room.
  #### d.1. On the EEG Measurement Computer:
  - Start a new file. 
    - Naming convention: "ExperimentName_DD-MM-YYYY_task_number". e.g., *EEG-tDCS_15-08-2021_stim_1*
    - Start *saving* the file
  #### d.2. On the Task Computer:
  - Run this command: `run_tay_eeg_experiment`
  - On the popup screen:
    - Choose "rest"
    - Choose the practice vs. task option
      - First try for all individuals is practice.
      - Next trials are all task.
    - Check the box "EEG recording started".
    - Press the button "Ready".
    - Close the pop-up.
  ----
  - Repeat the steps (0), 1, and 2 for all trials.