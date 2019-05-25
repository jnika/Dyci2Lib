# DYCI2_library

This library contains a collection of generative agents and tools for smart composition and human-machine co-improvisation. 
It integrates the results of the [DYCI2 project](http://repmus.ircam.fr/dyci2/home) and shapes a next-generation software with regard to [OMax](https://github.com/DYCI2/OMax4). A conference paper about the DYCI2 library can be downloaded [here](https://hal.archives-ouvertes.fr/hal-01583089/document).

This repository contains: 
* The __Max DYCI2 library__ of musical agents interfacing with the Python library. (See the tutorials in the directory _Max\_library/\_Tutorials\__ and the _Readme_ file to download sound examples).

* The __Python DYCI2 library__, defining models and tools for creative generation of sequences (and in particular musical sequences) from models of sequences. It implements several models, generative heuristics, time management strategies, and architectures of interactive agents. Each class is associated with a tutorial (see the tutorials in the _Python\_library_ directory).


__Author:__ Jérôme Nika (IRCAM STMS LAB);

__Contributors:__ Ken Déguernel (IRCAM STMS LAB / Inria Nancy - Grand Est), Axel Chemla--Romeu-Santos (IRCAM STMS LAB); 
__DYCI2 supervision :__ Gérard Assayag (Ircam, PI), Emmanuel Vincent (Inria Nancy, WP leader), Jérôme Nika (Ircam, WP coordinator), Marc Chemillier (EHESS, associate researcher).

__Some videos of collaborations with musicians using DYCI2 or its previous versions: https://www.youtube.com/channel/UCAKZIW0mMWCrX80yS96ZxAw__.

------
### Configuration, installations, and requirements

#### Python requirements
1. Download and install the **last** version of Python **2** (https://www.python.org/downloads).

2. Open Terminal to install the dependencies:

   `cd [DRAG_AND_DROP_THE_DIRECTORY_Dyci2lib]`
   
   `pip install -r requirements.txt`

(If _pip_ is not installed: `sudo easy-install pip`, or try `curl https://bootstrap.pypa.io/get-pip.py | python`)

#### Max externals
1. __Mubu for Max__, download from Max package manager. In Max:
	* File / Show Package Manager
	* Search "Mubu for Max"
	* Install
2. __Catart by Mubu__
	* Nothing to do if you downloaded a DYCI2 **release**.
	* [For developpers: if you **cloned** this reporitory or downloaded it from the main page, make sure that you also synchronised the [Catart](https://github.com/Ircam-RnD/catart-mubu) submodule or your directory `Dyci2Lib/Max_library/external/catart`will be empty !]

The last external, Antescofo, is already in the repository (please use the version distributed with DYCI2).

------
### Tutorials

Make sure that the path of the directory _Max\_library_ is set in the file preferences in Max.



The audio files corresponding to the Max tutorials can be downloaded here: http://repmus.ircam.fr/nika/dyci2_library. 

------
### Autonomous use of the Python modules

See the tutorials corresponding to the different modules. For example, in the directory _Python\_library_:

    `python Generator_tutorial.py`

Html doc: http://repmus.ircam.fr/downloads/docs/DYCI2_library/

PDF doc: in DYCI2lib/Python_library

------
### To create your own annotated musical memories

Use the __Max tutorial "A5"__ (_Max\_library/\_Tutorials\__).

Or:

1. Create a .csv / .txt annotation file with the following format:

* `start_date_event_1_in_ms` `;` `label_1_1` [SPACE] `...` [SPACE] `label_1_j`
* ...
* `start_date_event_i_in_ms` `;` `label_i_1` [SPACE] `...` [SPACE] `label_i_j`
* ...
* `date_end_file_in_ms` `;` `X`



2. Use the script `FromTextToDYCI2json_script` (__no "." or " " in the whole path of the file except for the extension__), for example:

	$ python FromTextToDYCI2json_script.py [path\_annotation\_file]

3. Move the _.json_ file and your _.aif_ sound file in _/MaxPatches/\_Tutorials\_/\_ExamplesCorpus\__


See the example of `Female-Voice-singing.csv` --> `Female-Voice-singing.json` (annotation for `Female-Voice-singing.aiff`).

N.B.: Some playing modes (scenarios of descriptors and reactive listening) do not require annotated files since they perform analysis and clustering automatically (see Max tutorials "B"). 

------
### C wrapper and OM/o7 library
* __libdyci2__: a C wrapper to the DYCI2 Python library allowing to compile libdyci2 as a dynamic library.
* __om-dyci2__: a library for using DYCI2/libdyci2 in the OM/o7 computer-aided composition environment.

are available at https://github.com/DYCI2/om-dyci2. 

------
### Notes
* Python2 (>=2.7, Python3 coming soon !)
* Max 8

------
### Development
Check the repository [DYCI2_library](https://forge.ircam.fr/p/DYCI2_library/)

------
### Troubleshooting
Please write to `jerome.nika@ircam.fr` for any questionsn and to share with us your projects using DYCI2 !

------
### License
GPL v3
