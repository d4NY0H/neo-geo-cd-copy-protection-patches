This is a collection of patches for all Neo Geo CD games that have copy protection. These patches are applicable to the current REDUMP and TOSEC ISO images.

The patches are in xdelta format and were created with DeltaPatcher. However, there are also other programs / cross-operating system options for applying the patches. Before patching, the checksum is checked to ensure that it is applied to the correct file. The file names contain the name of the file to be patched, the type of patch and the CRC32 checksum of the unpatched file.

The copy protection of the Neo Geo CD is based on 2 methods. Both methods are based on the fact that SNK has pressed faulty sectors onto the CD. These cannot be read 1:1 and are corrected by a CD-ROM drive.

1. The [CDZ] copy protection prevents the game from being started on the CDZ model only. The errors are located in the CPY.TXT file. The CDZ Bios checks whether the checksum of the CPY.TXT corresponds to the corrected value. It has become established practice to replace the first two occurrences of the letters “f” with “g”. This causes the copy to be regarded as the original again and the game starts.

2. The [IGP] copy protection is an in-game protection and only leads to a black screen and an error message after a while of playing. A code is then called up in the respective program file to check the originality. To prevent this, the subroutine must be exited before it is called. This can be implemented with a disassembler / hex editor. I have used the modified program files of FAKK2 from the “NGCD_Protection_Removal_Tutorial_1.0” for almost all patches. I checked them all individually in the disassembler beforehand. For some game revisions that have not yet been considered, I have modified them myself as a basis for the patches.

When using the NeoGeo CD SD Loader the [IGP] copy protection must have been removed. The [CDZ] copy protection does not apply there. But [CDZ] patched images have no negative effect either.