# Managing Chrome Browser with Intune for Windows

## Introduction
This project began as a solution to automate Chrome browser updates on user devices managed by Intune, eliminating the need to manually update each browser by navigating to **Help > About Chrome**. 

> **Note**: This guide assumes that Chrome is already deployed on your user devices via Intune. If you need a guide on deploying Chrome, let me know, and I can create a separate guide for that. In this guide, we'll focus solely on setting up policies to enable automatic updates.

## Requirements
To successfully apply Chrome policies for automatic updates, you will need:

- **Administrator Access**: Ensure you have an admin account to access the Microsoft Endpoint Manager admin center.
- **Chrome Version and OS Requirements**:
    - Chrome browser version **101** or later.
    - Windows 10 or Windows 11 (excluding Windows Home editions).
- **ADMX and ADML Templates**:
    - Templates for:
        - Windows
        - Google
        - Chrome
        - Chrome Update

## Steps

### Step 1: Import ADMX and ADML Templates
1. Import the ADMX and ADML files in the following order to avoid upload issues:
   - Windows
   - Google
   - Chrome
   - Chrome Update

### Step 2: Configure Your Policy
1. In the **Microsoft Endpoint Manager admin center**, navigate to:
   - **Devices** > **Windows** > **Configuration Profiles**.
2. Click **Create Profile**.
3. Set the following configuration options:
   - **Platform**: Select **Windows 10 and later**.
   - **Profile Type**: Choose **Templates**.
   - **Template**: Select **Imported Administrative templates (Preview)**.
4. Click **Create**.
5. Enter a name for the configuration profile, for example: `Imported Admin Templates - Google Chrome`.
6. Click **Next** to proceed with configuration.

### Step 3: Configure Browser Settings
1. Adjust Chrome browser settings according to your organization’s needs. For this guide, we’re enabling **automatic updates** for Chrome.
2. Define any **Scope Tags** as needed.
3. Click **Next**.

### Step 4: Assign Groups
1. Choose any relevant **Included Groups** and **Excluded Groups**, along with appropriate **Filters**.
2. Click **Next**.

### Step 5: Review and Create
1. Review the settings.
2. Click **Create** to apply the configuration.

Your Chrome browser settings are now managed through Intune, and auto-updates are configured based on your defined policies.

