# GNPS_Library_Tools
This is a Juptyer notebook serving to interact with a local installation of the Global Natural Products Social Molecular Networking (GNPS) tandem mass spectrometry library.

This was written to function on a Windows 10 installation of python v.3.9.13.

A list of the functions provided within the Jupyter notebook.
1. import_library(): Import the local installation of the GNPS library for access
2. retrieve_spectra(): Given a known ID of a spectra/compound within the library this function will find it and return the spectra with all of the associated metadata
4. retrieve_spectra_fast(): This function is identical to the retrieve_Spectra() function, but with the inclusion of the index of the GNPS ID name it can retrieve the spectra an order of magnitude faster
5. write_mgf(): This function will take the retrieved spectra and write it to a mascot generic format (mgf) file that is compatible with most open source mass spec tools. It only includes a minimal amount of metadata, but does an important function which increases the specificity of the compound mass from 2 decimal places to 5 decimal place. This improves molecular formula identifications in the SIRIUS program.
6. basic_substructure_search(): Given a SMILES string this function will search the entirety of the GNPS library for any known structures that contain that specific string within their own.
7. basic_mass_search(): Given a mass a ppm error range this will search the library for any compounds that are within the given range.
8. basic_name_Search(): Given a name for a compound this function will search the GNPS library for any compound names that are/contain any matched and return all matches up to the given number of matches (default=10).
9. display_spectra(): Given a retrieved spectra from retrieve_spectra or retrieve_spectra_fast this will plot the spectra in order to see the fragmentation pattern.
10. display_spectra_interactive(): This function will display the spectra in a way that can be interacted with, such as zooming and selecting.
11. display_structure(): Given a GNPS ID for a compound, this will search the library for the spectra match and then return an image of the chemical structure. If no structure is found it will say so and display the structure of serotonin (because sadness, lol)
