Themes v0.8
Updated October 15, 2009 by J-Factor

Send all feedback/comments/problems to plugins@j-factor.com



WHAT IS THEMES
===============================================================================

Dynamically change the theme of maps! Enjoy a dark night, sweeping storm or a
frosty blizzard without being forced to download another map. Modifiable
attributes include the skybox, lighting, fog, particles, soundscapes, color
correction and more.



VERSION HISTORY
===============================================================================

v0.8
	General
	- Really added convar "sm_themes_particles" this time
	- Modified plugin to force clients to download particle files for all
	  maps defined in the maps config. Warning: If you use this plugin with
	  custom maps be sure to make a <map name>_particles.txt file for them!
	- Possibly fixed color correction and particles sometimes not appearing
	  (the delay before they are applied at round start has been increased)
	- Added theme "Chilly" - enjoy a frosty and foggy morning!

v0.7
	General
	- Added convar "sm_themes_particles" to enable/disable custom particles

v0.6
	General
	- Some bug fixes

v0.5
	General
	- Initial testing release
	- Added everything


	
HOW DO I INSTALL?
===============================================================================

Copy everything EXCEPT fastdownload into your tf folder.
Copy the contents of fastdownload onto your fastdownload server.
Add the lines in add_to_pure_server_whitelist.txt to your
pure_server_whitelist.txt (located in your hl2 folder).

This plugin requires sv_pure 1 or lower!



WHAT ARE THE CONVARS?
===============================================================================

	sm_themes_version
		Themes version

	sm_themes_enable [0/1]
		Enables or disables Themes

	sm_themes_next_theme "theme-name"
		Forces the next map to use the given theme
		
	sm_themes_announce [0/1]
		Whether or not to announce the current/next theme

	sm_themes_particles [0/1]
		Whether or not to use custom particles



WHAT ARE THE CONFIG FILES?
==========================

All config files are located in "addons/sourcemod/configs/themes/"

	themes.cfg
		Defines the themes and their attributes.
		
	themesets.cfg
		Defines sets of themes and how they are selected.

	maps.cfg
		Defines the maps and what themesets they use.
	
	Read the comments at the top of the config files.
	


EXTRA INFO
===============================================================================

To support custom particles I've used a rather hacky method. Valve recently
added support for custom particles for maps by letting people create
<map name>_particles.txt files in the maps folder. What I do is create my own
file for each map containing the names of a bunch of custom particle files. I
do not overwrite the particles file of custom maps though.

The custom particle files are:
	/particles/custom_particles001.pcf
	/particles/custom_particles002.pcf
	...
	/particles/custom_particles500.pcf

Currently only 001 is used.


