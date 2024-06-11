v0.1.5 / 2018-04-06
==================
  * Updating README for some clarifications.
  * jshint added for linting, packages cleaned up
  * Added a bunch of older-but-since-lost procedural water shaders along with gerstner wave/wave cluster generation functions (all use UE4 engine content for textures, so hopefully no errors on that front now). Also removed some deprecated procedural shaders (including the former bad water one).
  * Updating all foliage shaders (standard and speedtree-related ones), updated material functions, updated the environment simulation material parameter collection, added some additional material functions, and added all generic textures for material placeholders.
  * Adding some new material functions: albedo tinting, three types of normal blending operations.
  * Updated NPM and then updated every package except gulp-watch's own reliance on gulp-util which gulp says should be removed.
  * Okay. Maybe this time the security warning box will go away forever.
  * Updating silly things because.
  * More potential security fixes maybe maybe?
  * Update package-lock
  * ... Okay. Actually fixed it this time.
  * Er. Properly addressed the security vulnerability in joy-create since, hey, it's handy to run npm update.
  * Merged feature/joy-create-v0.1 as the one in master is woefully out of date and the feature branch was stable last I checked (the old master branch version was vulnerable to a security vulnerability).
  * Merge branch 'feature/joy-create-v0.1'
  * Miscellaneous blend and layer fixes (though something still isn't adding up. Literally and figuratively.
  * Adding a first-pass at some rough material layers and blending functionality (based on car paints). It's... Not right yet, but it's something.
  * More updates to the speedtree shaders; some fixes here and there and also made the per-instance fade parameter a static switch option.
  * Rewrote the speedtree foliage shaders and added a new one for speedtree billboards. They are wonderful now.
  * Added a note on the unreliability of the object pooling code and made a Little Red Riding Hood metaphor for some reason.
  * Updates to the speedtree shaders based on iteration (after iteration (after iteration)) on Steel Hunters.
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public
  * Replaced m_shader_foliage_speedtree with m_shader_speedtree_foliage (along with some minor tweaks). Added m_shader_speedtree_foliage_body for foliage with wrapping textures (mostly bark/stems/etc.).
  * Updated the README.
  * Updated Joy Create in the README.
  * Added Joy Create with notes to the UE4 README.
  * Added procedural street/intersection tool plugin (from @ydrive).
  * Overhauled the speedtree foliage shader in conjunction with the new speedtree for UE4. Also fixed some albedo tinting/coloring issues in the standard shader. Tweaks to the standard POM shader.
  * Updated standard shader and added a POM shader (with *roughly* equivalent features to the standard shader).
  * Updates to the object pooling system (given some issues in the use of it with my test case).
  * Convert some debug print statements to Python3-style
  * Watch task bails out after setting up watches, so devstart can complete, although the gulp task will keep running since the watches themselves haven't ended
  * Add done-signalling to devstart, but something else is holding it up
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public
  * Updates to the standard shader.
  * joy-create work; removed codemirror in favor of monaco-editor, updated gulp to v4, cleaned up dependencies, started removing npm run-scripts in favor of proper gulpfile and task setup. Broke a lot of things.
  * Rename familyRoot to outputRoot, filenameRoot to inputRoot; closes #1
  * Revamped the markdown for this page so I didn't have to commit every stupid change individually.
  * Updated UE4 project conventions (todo: source asset conventions).
  * Yes, I'm dumb.
  * Updating markdown style to Ulysses'.
  * RenderDoc section needed a lower heading.
  * Forgot about the miscellaneous code snippets index link.
  * An extensive UE4 infostorm update on content creation (material-focused atm), rendering/shading skeleton, and graphics debugging.
  * Removed the asset library information into its own page; general UE4 info/resources-only here now.
  * Separating out asset information and "documentation" (lol) from the UE4 megafile.
  * Updating the license copyright year.
  * GitHub markdown lists are a pain in the ass.
  * Setup the page index.
  * Initial update to Unreal Engine 4 information and resources page.
  * Updated the metallic clearcoat shader with the customized fresnel term; cleanup on standard shader and tossed an alpha-masked standard shader in.
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public
  * Added IObjectPooling for any object using a pool to be able to override an instantiation method that will be used by the object pool for creating new instances.
  * I suck at formatting.
  * Added some information on the anamorphic lens flare code.
  * Very, very rough first pass anamorphic lens flare postprocessing effect (intended to be integrated into PostProcessing.cpp).
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public
  * Updating metallic and metallic-clear coat shaders.
  * More object pooling fixes.
  * Apparently had joy-create files I never checked in.
  * Fixed an occasional first-run crash with the pooling system.
  * The UE4 buildchain really likes piecemealing out those errors one-by-one, huh.
  * I swear, this object pooling thing was so much prettier and simpler when I started it. UHT/UE4 do not make non-UObject interfaces easy to deal with whatsoever.
  * Added UObjectPool::GenerateName for pool object creation time help.
  * UE4 didn't like my interface not inheriting from UObject so I did awful things to make the Unreal Header Tool believe that this was a legit setup (I crashed UHT a couple times). Anyway, pool should work now.
  * Why is it that the small, general classes are always the most nitpicky and complex. Renamed IObjectPooled::Destroy to ::DestroyInstance, so it doesn't conflict with actors/components' ::Destroy.
  * Added an ::Empty method to the object pooling system because... That's helpful. Argument to separate out instances that are still active. Removed auto-execution of IObjectPooled::Activate, as that's more useful to manually call. Added safety checks and asserts.
  * Prevent an infinite loop when deactivating a pooled object. Made IObjectPooled::Deactivate non-virtual. Reverted some code which assumed IObjectPooled was a UObject derivative.
  * Should probably remove the dependence on steelhunters.h as I'm willing to bet most people don't have that header.
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public
  * Added UObject-pooling interface and pool class functionality to ue4-source (NOTE: pool does not auto-add object instances if the pool fails to find a valid object; this is later work).
  * Er, misleading heading.
  * Cleaned up the UE4 base README document, added link to enum gist.
  * Fixed the broken-as-hell duplicate file logging PowerShell script.
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public into feature/joy-create-v0.1
  * Merging master.
  * YES. I FINALLY FIGURED OUT WHAT SYNTAX I WAS SUPPOSED TO USE.
  * More of me trying to figure out the syntax here.
  * About two minutes worth of work on getting the new structure to work.
  * Alternate electron setup for joy-create since, hey, my experience with javascript/node is entirely HEY WHAT DOES THIS DO *PRESS ENTER*.
  * Started maybe figuring more things out and structuring appropriately?
  * WHITESPACE CLEANING WOOOOO.
  * Reworked/styled/themed the electron window a bit, refactored things. Though I'm not sure what I refactored them into since I'm still figuring out what the hell is happening.
  * Got everything working slightly better than it did in the last check-in (less horrifying hacks).
  * Removing ace from the vendors/ subdirectory (it's handled in the install/postinstall step now). Added rimraf and vendor-copy to package.json.
  * Reworked the entire SHEBANG to be a bit more properly setup (except the mad dash to get the viewport working at the end). Got the three.js viewport working even though it's just pitch black. The editor pane isn't coorperating yet, but that's not far off.
  * Refactored files and filenames to make more sense; worked to get the old page working properly with the viewport/editor.
  * Updated the app, added webpack-dashboard telemetry support.
  * Setting up a proper procgen system (l-system, turtle placement, and first-order shapes). Also moving over to three.js. Nothing about this commit will work at all right now.

v0.1.1 / 2017-12-05
==================
  * Removed the tools subdirectory as the kernel generator was not anywhere near properly conceived (my fault).
  * Updated base repo README with change information for the UE4 assets.
  * Merge branch 'master' of https://github.com/joymachinegames/joymachine-public
  * - Adding updated UE4 assets (NOTE: created by 4.18; 4.17 assets are archived in a subfolder) and a PowerShell script for finding duplicate files recursively from a working directory.
  * Added a note that the UE4 assets are saved from UE 4.17.2, so anything lower won't jive.
  * Added Atrix256's random source code repo to the resources list.
  * Fixing note display.
  * Added the RESEARCH_PAPERS.md link.
  * Finally starting to list out research papers. Links forthcoming once I track down original sources.
  * Added a template ConsoleVariables.ini file to show what we use internally.
  * Clarifying the state of joy-create a bit better.

v0.1.0 / 2017-10-10
===================
  * WARNING: ue4 asset folder hierarchy will invalidate old assets. Changed the hierarchy/naming conventions for the ue4 asset folder. Which also means that I had to delete all the old assets or they would no longer work anyway, so this is kind of a clean slate. On the plus side: lot's of new, rewritten, tweaked, improved, added etc. material functions/shaders/etc.
  * Remove references to 'normal' in the do_saveas code, since it is not just for normals
  * Add 'rgb' texture build rule, which just copies the texture using the do_saveas function
  * Completely rewrote the master foliage shader, the material functions for handling wind, added an easy hue-saturation-luminance material function, and other fun stuff. Will document later.
  * Added a 'deletebranch' alias to help with deleting branches locally and remotely.
  * I also apparently REALLY wanted to handle the normal map case an extra time or so.
  * Balls. Forgot about the transparency/SSS map.
  * Fixed the albedo/normal maps being output as single-channel images. BOOSH. I KNOW PYTHON NOW.
  * Good news: I was right to think I was stupid and kind of fixed the python script (I don't know python). Bad news: normal maps are wonked up on output and the powershell script is all sorts of sideways bad.
  * Added support for opacity masks and subsurface (translucency) textures -- each as their own output. I haven't tested these changes yet, but what could go wrong.
  * Updated a bunch of material functions: `mf_truesky_directional_light` (which is actually a light function material), `mf_luminance`, `mf_radial_color`, and `mf_radial_normal`.
  * Forgot to add the trailing _ on the suffixes
  * Update readme for clarification
  * Megascan assembler has a dynamic strategy now and no longer generates RGBA textures because those were huge.
  * Actually for-realsies updating the README to reflect the state of the repo.
  * Adding information about joy-create.
  * Added email address.
  * Updated the RESOURCES page with some additional links.
  * Updated the speedtree master shader as well as the master triplanar one.
  * Added a material function for angle-based roughness; while this functionality exists at a high-level in UE 4.17, it doesn't allow for any customization.
  * Added the beginning of a new foliage master shader; it's... Costly. Maybe decent ideas, but not practical yet.
  * Moved joy-create back to the repo root as I want to give it some love during these painful SH build times lately.
  * Added a link to the RESOURCES.md page in the README.
  * Added syntax highlighting for shaders links.
  * Much, much more handy way to get environment variables (yay table wrapping).
  * Starting a general resources file; currently only has one link.
  * Added a powershell alias for printing out a file directory tree to a text file (it's handy, okay); needs a text file as its one and only argument.
  * Apparently mentions aren't a thing in READMEs.
  * Added TAA sharpening link.
  * Moved generate-changelog.ps1 to scripts-standalone subdirectory (scripts subdirectory is automatically searched/executed at startup if you use the existing powershell profile from this repo.
  * Moved generate-changelog.ps1 to the scripts folder. Like it should have been initially. If I wasn't dumb.
  * Added generate-changelog.ps1 and updated README.
  * Updating foliage and standard (+ standard metallic) master materials.
  * Moved jmkernels up a directory; renamed it to joy-kernels.
  * Create `CONTRIBUTING.md`
  * Create `CODE_OF_CONDUCT.md`
  * Added article link.
  * Updating the gitattributes template with DLL/PDB/LIB.
  * Documenting holy-fsck.
  * Added alias `holy-fsck`. What? It's useful.
  * Removed `git cl` as I didn't want to include things with dependencies.
  * Updating README with new aliases and colors/decorators.
  * Fixed the wonky tabs going on, what the hell, git.
  * Added get-extension-files to list all files of a given extension in a directory. Updated the sample powershell profile with some new commands.
  * Attribution is nice sometimes.
  * Stupid vi. No one likes vi.
  * Added an .inputrc for OSX/bash that make terminals... Much better.
  * Ignore .DS_Store on OSX.
  * Added an 's' alias for showing a colored, minimal git status
  * Removed specific folder filters for LFS; now blanket applied to UASSET/UMAP files.
  * Added a whole bunch of fancy new aliases to the gitconfig template.
  * Fixed the awful `mf_normal_lerp`. Updated `mf_wind` (and `mpc_world`).

v0.0.7 / 2017-07-23
===================

  * Adding v0.0.7 changelog.
  * Fixed mentor link to go to the site, not the repo for the site.
  * Added @ishansharma callout proper.
  * Added gamedev mentors link.
  * Add PNG compressor script.
  * Adding some additional powershell scripts/aliases.

v0.0.6 / 2017-07-05
===================

  * Fix bug that prevented sphere output from ever occurring.
  * Added Vector Field Generator (python), SmearFrame (UE4 material), reorganization.
  * Updating README to reflect v0.0.5 repo changes.

v0.0.5 / 2017-06-30
===================

  * Adding v0.0.5 change log.
  * Moved kernel generator and joy-create into a tools directory in the root folder.
  * Adding basic JSON serialization utility class (struct-oriented; UObject-based one is... Touchy still).
  * Moving .gitignore/attributes from kernel generator into root folder.
  * Provide pre-compiled release binary for jmkernels.exe
  * Moved the kernels app into this repository
  * Adding a batch file of limited-usefulness outside our terrain tile export process.
  * Updating README to reflect reorganized repo.
  * Improved distance fade material function; fade SSS on foliage over distance.
  * Add readme for `rename_images_by_timestamp.py`
  * Renamed `rename_by_timestamp.py` to `rename_images_by_timestamp.py`
  * Tweaks to python image rename script to use modified date + support JPG/GIF. Moved tools to scripts folder.
  * Add script to create copies of PNG files w/ filenames prefixed with their creation time (Windows only)
  * Added section on collision filtering.
  * Updated the sample PowerShell profile with some new alises for counting lines of code in a folder (*.h, *.cpp, *.cs) as well as clipboard manipulation.
  * Renamed scripts/vcmd to scripts/visualstudio. Added an extension to show full path of active file in status bar.

v0.0.4 / 2017-05-30
===================

  * Updated CHANGELOG.
  * Moved the powershell scripts into the scripts folder because... Well. I mean. It makes sense, yeah?
  * Added a VS extension (for VSCMD and the source VB file) for outputting a build time start/end timestamp as well as total time taken.
  * Added a simple overload of USpringArmComponent that can account for more than one ignored actor (the owner).
  * Adding mailmap to fix my name. This probably isn't supposed to be checked in.
  * Adding software link to the readme.
  * Removing dumb line.
  * Filling out AWESOME_SOFTWARE with... good... software?
  * Adding stub AWESOME_SOFTWARE.md file. Which I will then fill out on the computer that has the file.
  * Updated CHANGELOG for v0.0.3. I need to remember to do this before the tag.

v0.0.3 / 2017-05-27
===================

  * Adding AutoHotkey script for Windows' SnippingTool.
  * Words are hard.
  * Added a brief summary on the ue4-source folder.
  * Fixed up CollisionShapeSet. Added basic blueprintable enum for basic shapes.
  * General-purpose collision shape set for computing box/sphere/capsule shapes (rather than having to choose a specific one at code-time).
  * Even more convention updates as I read an awful class.
  * Added reference and link to the conventions doc.
  * Fixed sub-lists because I'm an idiot.
  * Greatly elaborated on the standard practices and conventions.
  * Consistency fix in the powershell folder.
  * Added an old material-based procedural water and wave generation/rendering asset set.
  * Actually changing the name of the folder in the README like I should have.
  * Removed "all rights reserved" heading.
  * Updated the UE4 general README with a link to the source control README.
  * Renamed git-template folder to git, since it's not just templates anymore.
  * Added even more specifics on customizing git for optimal everyday use.
  * Wrote a monologue on actors, components, and actor lifecycle.
  * Fix default camera
  * flip code and viewport panes
  * can load teapot, next up appending to the scene
  * Experimenting more with load code. Fixed broken IPC message handlers.
  * Figuring out how to handle events and OS integration, learning Electron as I go. Probably made a ton of mistakes.
  * make render-shell update when window is resized, take up entire pane
  * import babylon, create a test scene on the right pane
  * Added use information for the environment MPC and foliage shader.
  * Actually making the changelog reflect changes made.
  * Updated changelog for v0.0.2 release.

v0.0.2 / 2017-05-02
===================

  * Added an updated foliage standard shader that reads wind values from an MPC (in game_data/env).
  * Added a README.me file to the git-template gitconfig template.
  * Added two new aliases to the gitconfig.template added: git tree -- Just prints a pretty-formatted revision history in tree form. added: git cl -- NOTE: Required git-extras installed (for now). Generated a simple CHANGELOG based on commit log.
  * Added CHANGELOG.md link in the README.
  * Added a change log.
  * Made the root README suck marginally less.
  * Revamped `m_foliage_master` (just so happened to be working on our foliage today. COIIIINCIDENCE).
  * moved a lot of 3rd-party files into 'vendor' and also added babylon.js
  * Adding dumb changelog, but better than nothing. Still trying to find a good generator.
  * Additional information on PBR adherence.
  * Added information on the new standard shader library.
  * Adding our standard material library.
  * Removing the docs subfolder.
  * added the ACE js editor
  * add fancy icons to the buttons
  * touchups
  * quit on last window closed, even on macosx
  * master-detail demo layout
  * add css, fonts from photon UI framework
  * readme update
  * revised readme
  * electron-quick-start shell added

v0.0.1 / 2017-04-30
===================

  * Tweaks to the 'git state' alias.
  * Added .gitconfig template with state and last aliases.
  * Added batch file for renaming branches on local and remote git repos. Will eventually be replaced with a git alias.
  * Replaced the Content/char directory with Content/mech.
  * Added material-related naming conventions.
  * Updated the materials library. added: `mf_distance_fade` (kind of what it sounds like). added: `mf_fresnel_gradient` (this may not work at the moment). added: `mf_fuzzy_shading` (more customizable version of Epic's fuzzy shading function). added: `mf_highprecision_worldpos_sampling` (I hope it's what it sounds like because I don't remember even writing it). added: `mf_luminance_adaptive` (calculates the luminance of a single buffer sample, optionally taking eye adaptation into account). added: `mf_metallic_shading` (exaggerated shading for metallic materials; based on Epic's with iterations on our side). added: smooth step material function; changed scalar-based one based on research, float3 one is pretty standard. added: SRGB->Linear color conversation using a best-fit value. added: A whole lot of texture bombing functions in order to split out the complexity from Epic's one-stop-shopping one. Note: still very expensive. added: `mf_truesky_directional_light` (just a copy of trueSKY's shadow mapping function). added: mf_wind (gets a float4 from a material parameter collection and uses the X/Y as wind direction and W as wind speed). added: the miscellaneous post-effect sharpening materials I've been playing with.
  * Misc. updates and fixed the list views.
  * Updated CONVENTIONS.md with some filename prefixes.
  * Created CONVENTIONS.md and got it kinda started.
  * Fleshing out the README.md with informations!
  * Tried adding Sign Bunny to the greeting. Failed.
  * Adding some UE4 assets that I dig.
  * Adding git attribute/ignore/LFS templates.
  * Updated INSTALL instructions.
  * Updated powershell script installation instructions with a note that I'm an idiot.
  * Adding PowerShell 5 scripts/tools, a sample profile, and setup instructions.
  * Added tool to automate channel-packing for megascan textures.
  * More export artifact clean-up.
  * Fixed some basic export artifacts from Notion.
  * I'm dumb.
  * Fixing up the header.
  * Adding in our internal Todoist task management practices doc.
  * Updated the README with a better header.
  * Initial commit
