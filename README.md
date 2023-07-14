# GNPS_Library_Tools
This is a Juptyer notebook serving to interact with a local installation of the Global Natural Products Social Molecular Networking (GNPS) tandem mass spectrometry library.

This was written to function on a Windows 10 installation of python v.3.9.13.

A list of the functions provided within the Jupyter notebook.
1. import_library(): Import the local installation of the GNPS library for access\n
2. retrieve_spectra(): Given a known ID of a spectra/compound within the library this function will find it and return the spectra with all of the associated metadata
4. retrieve_spectra_fast(): This function is identical to the retrieve_Spectra() function, but with the inclusion of the index of the GNPS ID name it can retrieve the spectra an order of magnitude faster
5. write_mgf(): This function will take the retrieved spectra and write it to a mascot generic format (mgf) file that is compatible with most open source mass spec tools. It only includes a minimal amount of metadata, but does an important function which increases the specificity of the compound mass from 2 decimal places to 5 decimal place. This improves molecular formula identifications in the SIRIUS program.
6. basic_substructure_search(): 
