path: tree/master/docs/faq
source: faq.md

# Frequently Asked Questions
## What is the blue box?
The blue box is a diagnostics tool for the fctl2 branch, currently running on the Cygnus channel. It's important, and no, you can't turn it off.

## Why does the updater say it is "locked for maintinence"?
In general, there are 2 reasons:
* We're actively shipping an update, which takes time - just wait until later
* There are no updates available on that branch

It is **not** possible to upgrade from 1.4.x to 1.5.0 using the updater. You need to reinstall the 787 from the store.

## When will ... update release?
When it's ready...

## What is Cygnus?
Cygnus is the name for our updater-based public beta program. It is not designated as stable, so should only be used if you are comfortable with identifying and reporting bugs. It can be enabled or disabled using the Skunkcraft's Updater "Enable beta channel" box

## What is Discord?
We use Discord as our primary means of communication and support for customers. You can access our server at https://magknight.org/discord

## My serial key has run out of activations
If your key has run out of activations, you can contact us on the forums, social media or by email to add more activations.

## How do I enable rain effects?
Rain effects, provided by librain are enabled in the EFB's settings page. The setting is located on page 2.

## How do I trigger cabin announcements?
Announcements are operated from the COMM pages within the MFDs. To activate this page, click COMM on one of the MFD control sets, then click CABIN. 

## Why are my MCP/Radios screens black?
When starting from cold and dark, the MCP and Pedestal backlighting is turned to minimum setting. This rotary knob also controls the screen brightness of the MCP and radios. 
To turn on the radios, turn the AISLE STAND PNL rotary to the full right setting; It's located at the back right of the pedestal.

To turn on the MCP, turn the GLARE PNL rotary to the full right setting; it's located on the bottom-left of the overhead panel.

## Does the 787 support MacOS?
Yes, it does! You'll need to update it to 1.2.10 or later to get support

## The 787's fuel consumption is far too low
Make sure you have "Experimental flight model" **disabled** in the x-plane settings. We don't provide support for the experimental flight model at this time.


## How do I update my 787?
With the **787**: Aviator's Edition comes the ability to auto-update your aircraft using the SkunkCrafts updater. Minor updates (1.0.x) will only be shipped through these means.

The SkunkCrafts updater can be found [here](https://forums.x-plane.org/index.php?/forums/topic/144828-updater-download-page-v22-available/).

You'll find the changelog in your aircraft's folder.

Missing the config file? Download it [here](https://docs.magknight.org/img/skunkcrafts_updater.zip). You'll need to place it in your aircraft's root directory.

## What does VATSIM mode do?

!!! warning "Legacy"
    VATSIM mode has been removed in the release version of 1.5.0 - it's functionality is mostly replaced by ACARS

VATSIM mode enables intergration with the [VATSIM network](https://vatsim.net). It enables SELCAL identification, radio uplink using contact-me messages, and some other uplink-related features. *VATSIM mode only works with X-Squawkbox; due to a lack of dataref availablilty, the Swift pilot client, and IVAO clients are not supported*

## Do old liveries work on 1.5.0?
Liveries released since 1.4.0 **will** work with 1.5.0, however we have shipped an updated paintkit with 1.5.0, containing new tail and wing texturing, some fuselage changes and the SATCOM dome. Liveries will need to be updated to the new paintkit to benefit from these improvements, but won't stop working. Aditionally, liveries will need updates to take advantage of the new GE and RR engine models shipped with 1.5.0

## How do I switch engine types?
Go to the EFB settings page, and find the **ENGINE TYPE** setting. Liveries should ship with an updated liverySettings file that defines the engine type(s) supported by it.

## How do I switch between 1.4.0 and 1.5.0 GE engines?
Go to the EFB settings page, and find the **LIVERY VERSION** setting. Liveries should ship with an updated liverySettings file that defines the engine type(s) supported by it.

## Does the 787 work in VR?
We don't directly support VR, and haven't made any special arrangements to allow it to work. Many users have however reported that the plane does work in VR.

We recommend these modifications if you'd like to use the plane in VR:

- [VR hotspots for cockpit seats](https://forums.x-plane.org/index.php?/forums/topic/172655-vr-hotspots-for-cockpit-seats/) by [Xplaner-73](https://forums.x-plane.org/index.php?/profile/428045-xplaner73/&wr=eyJhcHAiOiJmb3J1bXMiLCJtb2R1bGUiOiJmb3J1bXMtY29tbWVudCIsImlkXzEiOjE3MjY1NSwiaWRfMiI6MTYwMjY4OX0=) (X-Plane.org)
- [MoveVR](https://forums.x-plane.org/index.php?/files/file/44809-movevr-move-external-windows-into-x-plane-even-into-vr/) by [Folko](https://forums.x-plane.org/index.php?/profile/215470-folko/&wr=eyJhcHAiOiJkb3dubG9hZHMiLCJtb2R1bGUiOiJkb3dubG9hZHMiLCJpZF8xIjo0NDgwOX0=) (X-Plane.org)
