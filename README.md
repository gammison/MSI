# MSI
## Current Project Structure

### Usage:

Example Pruning in a python prompt:
''' Python
Python 3.6.5 |Anaconda, Inc.| (default, Apr 29 2018, 16:14:56) 
[GCC 7.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import MSI.cti_core.cti_processor as pr
>>> test_processor = pr.Processor('./MSI/data/test_data/FFCM1.cti')
>>> test_processor.prune('./MSI/cti_core/testind')
Error on index 5say
: invalid literal for int() with base 10: '5say'
 Skipping index
remove index 1, reaction H + O2 <=> O + OH
remove index 2, reaction H2 + O <=> H + OH
remove index 3, reaction H2 + O <=> H + OH
>>> test_processor.prune(3)
remove index 3, reaction H2 + M <=> 2 H + M
>>> test_processor.prune([1,4,77])
remove index 1, reaction H + O2 <=> O + OH
remove index 4, reaction H2 + HE <=> 2 H + HE
remove index 77, reaction CH2(S) + H2O2 <=> CH3O + OH
>>> test_processor.write_to_file()
'./MSI/data/test_data/FFCM1_processed.cti'
>>> exit()
'''
