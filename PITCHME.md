---?image=assets/images/gitpitch-audience.jpg
@title[Title-UEFI Overview]
<br><br>
<span style="font-size:0.75em" >This slide deck has moved to:  https://gitpitch.com/tianocore-training/EDK_II_Build_Spec_Files_Pres/master#/</span>
<br><br><br>
## <span class="gold"   >&nbsp;UEFI & EDK II Training</span>

####  &nbsp;&nbsp;EDK II Build Specification Files
<br>
<span style="font-size:0.75em" >&nbsp;&nbsp;&nbsp;<a href='http://www.tianocore.org'>tianocore.org</a></span>
Note:
  PITCHME.md for UEFI / EDK II Training EDK II Build Process

  Copyright (c) 2018, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



---  
@title[Lesson Objective]
<br>
### <p align="center"<span class="gold"   >Lesson Objective </span></p><br>
<br><br>
<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
 @fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Explain the Build components and Build text files: <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DSC, DEC, & FDF </span><br><br>
 
---?image=assets/images/binary-strings-black2.jpg
@title[EDK II Overview Section]
<br><br><br><br><br>
## <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EDK II Build Text files </span>
<span style="font-size:0.9em" > &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The EDK II Specification: DEC, DSC & FDF files </span>




+++
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->		  
@title[EDK II File Extensions]
<p align="center"><span style="font-size:1.0em" > &nbsp;&nbsp;&nbsp;<font color="#e49436"><b>EDK II File Extensions</b></font></span>
<span style="font-size:0.7em" ><font color="white"><br>-&nbsp;Located on <a href='http://www.tianocore.org'>tianocore.org</a> project edk2  </font> </span></p>


<table id="recTable">
	<tr>
		<td bgcolor="#121212"><p style="line-height:70%"><span style="font-size:0.75em" ><b>@color[#00ffff](.DSC) <br>.DEC &nbsp;&nbsp;<br>@color[#00ffff](.INF)<br>.FDF</b></span></p></td>
		<td bgcolor="#121212"><p style="line-height:70%"><span style="font-size:0.75em" ><b>@color[#00ffff](- Platform Description ) <br>- Package Declaration <br>@color[#00ffff](- Module Definition <i>define a component</i>) <br>- Flash Description </b></span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:50%"><span style="font-size:0.65em" >.VFR <br>.UNI <br>.c & .h </span></p></td>
		<td bgcolor="#323232"><p style="line-height:50%"><span style="font-size:0.65em" >- Visual Forms Representation for User interface <br>- Unicode String text files w/ ease of localization<br>- Source code files</span></p></td>
	</tr>
	<tr>
		<td bgcolor="#323232"><p style="line-height:50%"><span style="font-size:0.65em" >.FD <br>.FV </span></p></td>
		<td bgcolor="#323232"><p style="line-height:50%"><span style="font-size:0.65em" >- Final Flash Device Image  <br>- Firmware Volume File</span></p></td>
	</tr>

</table>

@snap[north-east span-30]
@css[ text-yellow fragment](<span style="font-size:01.45em" ><b><i><br><br>&nbsp;@color[yellow](EDK II Spec)<br><br><br>&nbsp;@color[yellow](Source)<br><br>&nbsp;@color[yellow](Output)</i></b> </span>)
@snapend
  
 

Note:
So for file extensions <br>

-So first we have a DSC file this is for platform description. This is an extension of the existing DSC file from EDK 1.  This describes the build rules, libraries and components that are going to get Built. 
-We have the DEC file which is the Package Declaration. Each package has a package declaration or DEC file, and it declares all the interfaces that the package has.  This is one of the new files
Next we have INF file 	- Module Definition this is a description of one module and what it has
Next we have a FDF file -Flash Description File – this information used to be part of the original DSC file but has been split off into a new file. This describes which module or modules weather it was built as part of the DSC or included in a binary – it describes which module gets to go where in the flash – which one is comprised – which one goes in to recover - it is a or mapping of the flash device –
Next we have a DXS file which is a Dependency expression file -  this is used by the DXE and in PEI modules to Define what prerequisites they have before they can run
Finally we have the FV file - Firmware Volume image file - 
 
First four have a specification file located on tianocore.org.

See EDK II Build Specification Documentation: 
          http://tianocore.org/  
		  

---?image=/assets/images/slides/Slide5.JPG
<!-- .slide: data-transition="none" -->		
@title[Build Description File Types ]
#### <p align="right"><span class="gold" >Build Description File Types </span></p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<span style="font-size:0.8em" >wiki Link on tianocore.org<br>
<a href='https://github.com/tianocore/tianocore.github.io/wiki/Build-Description-Files'>Build Descrip Files</a></span>	

Note:
INF defines all required information for a single item (source file information and dependencies).
DEC declares interfaces available from package
Includes, GUIDs, Protocols, PPIs, and PCDs
DSC describes what needs to be built from sources
FDF describes how to package built output and binaries into the flash device

Parsing stage
Flash tool stage

Each file type has spec on EDK II website … Tianocore.org

+++?image=/assets/images/slides/Slide6.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Build Description File Types 02 ]
#### <p align="right"><span class="gold" >Build Description File Types </span></p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<span style="font-size:0.8em" >wiki Link on tianocore.org<br>
<a href='https://github.com/tianocore/tianocore.github.io/wiki/Build-Description-Files'>Build Descrip Files</a></span>	

Note:
INF defines all required information for a single item (source file information and dependencies).
DEC declares interfaces available from package
Includes, GUIDs, Protocols, PPIs, and PCDs
DSC describes what needs to be built from sources
FDF describes how to package built output and binaries into the flash device

Parsing stage
Flash tool stage

Each file type has spec on EDK II website … Tianocore.org

+++?image=/assets/images/slides/Slide7.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Build Description File Types 02 ]
#### <p align="right"><span class="gold" >Build Description File Types </span></p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<span style="font-size:0.8em" >wiki Link on tianocore.org<br>
<a href='https://github.com/tianocore/tianocore.github.io/wiki/Build-Description-Files'>Build Descrip Files</a></span>	

Note:
INF defines all required information for a single item (source file information and dependencies).
DEC declares interfaces available from package
Includes, GUIDs, Protocols, PPIs, and PCDs
DSC describes what needs to be built from sources
FDF describes how to package built output and binaries into the flash device

Parsing stage
Flash tool stage

Each file type has spec on EDK II website … Tianocore.org

---?image=/assets/images/slides/Slide9.JPG
@title[Package Declaration File]
#### <p align="right"><span class="gold" > Package Declaration File (DEC)</span></p>

Note:
One DEC file per package
Required for EDK II modules using extended INF and extended DSC format files 

The “ D” in DEC stands for “declaration”, as in package declaration file (DEC).
There is one DEC file for each package.
This file is required for using EDK II modules using the extended INF and extended DSC format files. 
If you make a new package you must have a DEC file for it.
SYNTAX -
The DEC has a defines section that says what this package is. It gives it a GUID and a name. Every other section described here is optional. 
It can have an includes section words saying “the include directories that this package has are as follows”. Then you would have some include directories. For example, you might be able to say this is my IA64 include and this is my X64 include, etc.
It has a library class section (optional). This exposes the library classes are defined in this package.
It has GUID section if there are any GUIDs that you have. Certain structures have GUIDs defines for them. If that structure is defined in this package, it would be listed there.
Each protocol for every protocol header file that is in your package you list.  You list the GUID of that protocol in the protocol section.
The same is true for PPIs; they are also identified by GUID.
PCD, if any module contained in your package defines a new PCD, this is where you tp look it up.
It is possible to reference a PCD from another package, but do not list it here. This location is for new PCDs.
Coincidentally,  as soon as you make a new PCD, you must make a new token space GUID, because all the PCDs are defined by a token space GUILD, followed by the PCD name. A new token space means you must have a GUID for the token space. So, any new PCDs are also going to have a GUID.
Finally, user extensions are rarely used but are optionally present. 



---?code=sample/OvmfPkg/OvmfPkg.dec&lang=shell&title=Example: DEC file

Note:
This is an Example DEC File

The name of this package is the Ovmf package. It has some GUIDs. In the includes.common section there is an include directory for this package called include, and that is where to locate all of the include files. 
In this example it finds a library class called LoadLinuxLib . The main interface for that is that it includes “Include/Library/  .h” 
We can see that it defines a GUID called “gUefiOvmfPkgTokenSpaceGuid” and it defines what the GUID value is.

Restrictions 
It is NOT permissible to list a Library Class entry under common and under a specific architecture. It is permissible to specify Library Class entries under all architectures except “common” if different header filename values are required for different architectures. 
Paths cannot contain indirect directory references outside of this package's directory tree (use of “..” is not allowed in a directory path name.)

+++?code=sample/OvmfPkg/OvmfPkg.dec&lang=shell&title=Example: DEC file details

@[16-20](List of Defines,  Package Name, GUILD, Version ...)
@[22-23](The Include section,there is an include directory for this package )
@[25-37]( Library classes section, these are the libraries created by this package. Notice each is pointing to a .h file )
@[59-65]( Guids section, Guids defined by this package)
@[67-73]( Protocols section, Porotocols defined by this package)
@[74-82]( PCDs Section, Declared by this package)
@[111-120]( Dynamic PCDs Section, Declared by this package)
@[140-153]( Feature flag PCDs Section, Declared by this package)


Note:
This is an Example DEC File

The name of this package is the Ovmf package. It has some GUIDs. In the includes.common section there is an include directory for this package called include, and that is where to locate all of the include files. 
In this example it finds a library class called LoadLinuxLib . The main interface for that is that it includes “Include/Library/  .h” 
We can see that it defines a GUID called “gUefiOvmfPkgTokenSpaceGuid” and it defines what the GUID value is.

Restrictions 
It is NOT permissible to list a Library Class entry under common and under a specific architecture. It is permissible to specify Library Class entries under all architectures except “common” if different header filename values are required for different architectures. 
Paths cannot contain indirect directory references outside of this package's directory tree (use of “..” is not allowed in a directory path name.)


---?image=/assets/images/slides/Slide15.JPG
@title[Package Description File]
#### <p align="right"><span class="gold" > Package Description File (DSC)</span></p>

Note:

- DSC file must define all libraries, components and/or modules that will be used by one package
- DSC files are a list of: 
  - EDK Component or EDK II Module INF Files   
  - EDK libraries (for EDK Components) 
  - EDK II Library Class Instance Mappings (for EDK II Modules) 
  - EDK II PCD Entry Settings  


---
@title[Platform Description File ]
#### <p align="right"><span class="gold" > Platform Description File (DSC)</span></p>

<p align="center"><span style="font-size:1.20em" > <font color="#00FFFF">DSC file is the recipe for creating a package</font></span></p>
@ul[no-bullet]
-  <p align="center"><font color="#FFFF00">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Definitions for the package build </font> </p> 
-  <p align="center"><font color="#ffff99">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EDK libraries (for EDK Components)  </font> </p> 
-  <p align="center"><font color="#87E2A9">&nbsp;&nbsp;EDK II Library Class Instance Mappings (for EDK II Modules) </font> </p> 
-  <p align="center"><font color="#FFC000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EDK II PCD Entry Settings  </font> </p> 
-  <p align="center"><font color="#00FFFF">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;EDK Component or EDK II Module INF Files</font> </p> 
@ulend


Note:
DSC file must define all libraries, components and/or modules that will be used by one package


---?code=sample/OvmfPkg/OvmfPkgX64.dsc&lang=shell&title=Example: DSC file
Note:
This is an example DSC file

+++?code=sample/OvmfPkg/OvmfPkgX64.dsc&lang=shell&title=Example: DSC file details



@[22-32](List of Defines,  Package Name, GUILD, Version ...)
@[33-41]( Define Switches to deterimine some configurations )
@[62-74]( Build Options)
@[106-115]( Library Classes - Global. Notice the DSC file is pointing to the .inf file )
@[404-421]( PCDs Section, changing the default value by this package)
@[502-520]( Dynamic PCDs Section, changing the default value by this package)
@[557-571]( Finally the Components section, which every DSC MUST have)


Note:
This is an example DSC file

---?image=/assets/images/slides/Slide21.JPG
@title[Flash Description File ]
#### <p align="right"><span class="gold" > Flash Description File (FDF)</span></p>

Note:
- FD section defines for Flash devices must be in the FDF file
- FV – section defines firmware Volumes must be in FDF file

- The FDF file
- This describes information about the flash part.
- It has rules for combining binaries built from a DSC file.
- You can create firmware images option ROM images for nearly anything you needed.
- It is possible to have the PCD information used in the definition, and also in some of the PCDs. The patchable ones will be stored at specific places inside the FV file. 
- Syntax:
- The FDF file has 
- a header and 
- a defines, 
- a FD section, 
- some number of FV sections.
- It might have a capsule,
- a VTF, rules, 
- an option ROM section if what you are trying to build is a PCI option on
- some user extensions. 



---
@title[Flash Description File ]
#### <p align="right"><span class="gold" > Flash Description File (FDF)</span></p>
<br>
@ul[no-bullet]
- <p align="center"><font color="#FFFF00">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Describes information about flash parts</font> </p> 
<br>
- <p align="center"><font color="#00FFFF">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Used to create firmware images, Option ROM images or bootable images </font> </p> 
<br>
- <p align="center"><font color="#A6C639">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Rules for combining binaries (Firmware Image) built from a DSC file</font> </p> 
@ulend

Note:
- FD section defines for Flash devices must be in the FDF file
- FV – section defines firmware Volumes must be in FDF file

- The FDF file
- This describes information about the flash part.
- It has rules for combining binaries built from a DSC file.
- You can create firmware images option ROM images for nearly anything you needed.
- It is possible to have the PCD information used in the definition, and also in some of the PCDs. The patchable ones will be stored at specific places inside the FV file. 
- Syntax:
- The FDF file has 
- a header and 
- a defines, 
- a FD section, 
- some number of FV sections.
- It might have a capsule,
- a VTF, rules, 
- an option ROM section if what you are trying to build is a PCI option on
- some user extensions. 

---?image=/assets/images/slides/Slide24.JPG
<!-- .slide: data-transition="none" -->
@title[Flash Description File Layout ]
#### <p align="right"><span class="gold" > Flash Device Configuration Common <br> Layout File (.fdf)</span></p>

Note:

+++?image=/assets/images/slides/Slide25.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Flash Description File Layout 02]
#### <p align="right"><span class="gold" > Flash Device Configuration Common <br> Layout File (.fdf)</span></p>

Note:

+++?image=/assets/images/slides/Slide26.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Flash Description File Layout 03]
#### <p align="right"><span class="gold" > Flash Device Configuration Common <br> Layout File (.fdf)</span></p>

Note:

+++?image=/assets/images/slides/Slide27.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Flash Description File Layout 04]
#### <p align="right"><span class="gold" > Flash Device Configuration Common <br> Layout File (.fdf)</span></p>

Note:

+++?image=/assets/images/slides/Slide28.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Flash Description File Layout 05]
#### <p align="right"><span class="gold" > Flash Device Configuration Common <br> Layout File (.fdf)</span></p>

Note:

+++?image=/assets/images/slides/Slide29.JPG
<!-- .slide: data-background-transition="none" -->
<!-- .slide: data-transition="none" -->
@title[Flash Description File Layout 06]
#### <p align="right"><span class="gold" > Flash Device Configuration Common <br> Layout File (.fdf)</span></p>

Note:
---?code=sample/OvmfPkg/OvmfPkgX64.fdf&lang=shell&title=Example: FDF file

+++?code=sample/OvmfPkg/OvmfPkgX64.fdf&lang=shell&title=Example: FDF file details

@[19-35](List of Defines,  defines the main macros and sets the dependent PCDs.)
@[99-108]( The FD Section - produces a file OVMF.FD in the build outputs directory )
@[110-132]( Begin the Variable Storage Regions - Layout Regions that define an empty variable store. NV Vars, Event Log, FTW regions defined)
@[220-225]( Firmware Volumes that are going to be created )
@[282-301]( Now define what goes inside the SEC Firmware Volume)
@[303-312]( We see that SecMain and the reset vector are defined)
@[314-336]( Now define what goes inside the PEI Firmware Volume  and etc...)
@[612-624]( Rules section for determining how to combine binary images, for example compression algorithms)
@[19-719]( Showing the whole FDF file again)



Note:
This is an example FDF file

---  
@title[Lesson Summary]
 
<br>
### <p align="center"<span class="gold"   >Summary</span></p><br>
<br><br>
<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
 @fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Explain the Build components and Build text files: <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DSC, DEC, & FDF </span><br><br>
 

<!---  END OF SLIDES
-->

---?image=assets/images/gitpitch-audience.jpg
@title[Questions]
<BR>
![Questions](/assets/images/questions.JPG =10x) 


---?image=assets/images/gitpitch-audience.jpg
@title[Logo Slide]
<BR><BR><BR>
![Logo Slide](/assets/images/TianocoreLogo.png =10x)

---  
@title[Backup]
<br><br><br><br><br>
### <p align="center"<span class="gold"   >Backup </span></p>

---
@title[Acknowledgements]
<br>
#### <p align="center"<span class="gold"   >Acknowledgements</span></p>

```c++
/**
Redistribution and use in source (original document form) and 'compiled' forms (converted
to PDF, epub, HTML and other formats) with or without modification, are permitted provided
that the following conditions are met:

Redistributions of source code (original document form) must retain the above copyright 
notice, this list of conditions and the following disclaimer as the first lines of this 
file unmodified.

Redistributions in compiled form (transformed to other DTDs, converted to PDF, epub, HTML
and other formats) must reproduce the above copyright notice, this list of conditions and 
the following disclaimer in the documentation and/or other materials provided with the 
distribution.

THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR IMPLIED 
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND 
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL TIANOCORE PROJECT BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES 
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, 
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF ADVISED OF THE POSSIBILITY 
OF SUCH DAMAGE.

Copyright (c) 2018, Intel Corporation. All rights reserved.
**/

```
