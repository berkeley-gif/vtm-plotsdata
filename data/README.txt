*** VTM PLOT DATA ***

Wieslander Vegetation Type Mapping Project
College of Natural Resources
University of California, Berkeley

** QUAD N60  **
EXPORTED FROM DATABSE ON Tue, 23 May 2006 17:09:02 PDT

The plot data consist of about 18,000 datasheets of recorded vegetation and 
environmental data from plots located throughout California and nearby areas of 
Nevada and Oregon. Most plots were recorded in the 1930's and some as early as 
the 1920's.  The plot data were entered into a relational database from which
the files in this archive were exported.

Fields ending in "_lump" are revised versions of the corresponding 
original fields that have been formatted to minimize inconsistency in the 
original data.  These corrected fields should be easier to use in analysis, but 
we provide the original data as well for validation.

Some of the species codes used in the Wieslander VTM Project are ambiguous due 
to missing documentation, lack of quad-specific code-to-name translations, or 
conflicting translations We attempt to report this ambiguity in all of our data 
products, but please take extra care when performing analysis based on these 
codes.  For a full list of codes associated with multiple possible species, see 
http://vtm.berkeley.edu/about/ambiguous.php


For more information on the plot data, please visit 
http://vtm.berkeley.edu/about/
To download GIS data of plot locations, please visit 
http://vtm.berkeley.edu/data/


** FILES **

plotdata-plot

  Non-vegetative metadata collected by the original VTM surveyors.
  
  *Fields*

  PID                                     
    Primary key

  PLOTKEY                                 
    Combination of map number and plot number, without spaces or dashes.

  PLOT_ID                                 
    An automated number that was assigned to each datasheet entered in the
    database.

  MAP                                     
    Plot map number as written on datasheet.

  PLOT_NO                                 
    Letter and number combination written in red ink at top of front page on
    datasheet.  Corresponds to location on plot map.  For example, A-1-1
    plot number is located in the A1 section on the plot map, and is located
    where the circled 1 is written in this section.

  QUADRANGLE                              
    Name of quadrangle as written on the datasheet.

  GEOGRAPHIC_LOCATION                     
    Plot location as written on datasheet.

  FD_DATE                                 
    Date as written on datasheet.

  SECTION                                 
    Section number as written on datasheet.

  TOWNSHIP                                
    Township as written on datasheet.

  RANGE                                   
    Range as written on datasheet.

  TAKEN_BY                                
    Field recorder's name, usually entered as written on datasheet.

  EXPOSURE                                
    Plot exposure as written on datasheet, either as abbreviation of
    cardinal direction or as the name of the direction (For ex.
    "Southerly").

  SLOPE_PERCENT                           
    Numerical percent slope of plot as written on datasheet (unless written
    as text).

  ELEVATION                               
    Elevation in feet of plot as written on datasheet.  This field had an
    upper bound of 15,000 ft.

  YEAR_OF_LAST_BURN                       
    Year of last burn as written on the datasheet.

  SITE                                    
    Site as written on the datasheet.  Site index is average dominant tree
    height at 300 years.   It is estimated to the nearest 25 foot class,
    from 75 to 225.  For example, site index of 75 indicates that the
    average dominant tree height at 300 years is about 75 feet.  Entries for
    this field can include &#8220;NT&#8221;, meaning non-timber, or
    &#8220;NC&#8221;, meaning non-commercial, instead of the Site Index
    number.  VTM field personnel determined the site index using increment
    cores to date the age of the tree and site index curves specific to the
    tree species (see The Manual of Field Instructions pp. 9-11 for more
    information).

  PENETRABILITY                           
    Penetrability as written on the datasheet.

  PARENT_ROCK                             
    Parent rock type of the soil as written on the datasheet.

  SOIL_DEPTH                              
    Soil depth as written on the datasheet.

  SOIL_ROCKY                              
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  SOIL_GRAVELLY                           
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  SOIL_SANDY                              
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  SOIL_LOAM                               
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  SOIL_SILT                               
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  SOIL_CLAY                               
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  SOIL_ADOBE                              
    Boolean soil character field, corresponding to the Soil Character
    checkboxes on the datasheet.

  EXCESSIVE_EROSION_EVIDENCE              
    Excessive errosian evidence as written on the datasheet.

  ADDITIONAL_GROUND_COVER_SPECIES         
    Each species or species code was entered on a separate line in this
    field.  Species names and species codes were entered as written on
    datasheet.  Abundance information for a particular species ("x" or "xx"
    or "xxx", etc.) was entered after the species name or code and on the
    same line, with either a space or a hyphen between the species name and
    its abundance.  Although this was the policy, data enterers sometimes
    entered the abundance information ("x", "xx", etc) before the species
    name, as written on the datasheet.

  SPECIAL_FIRE_HAZARDS                    
    Special fire hazards as written on the datasheet.

  REMARKS                                 
    Original VTM surveyor remarks as written on the datasheet.

  MISCELLANEOUS_NOTES                     
    The Miscellaneous_Notes field includes both actual data recorded at time
    of the original VTM survey as well as 2004 data enterers' comments about
    the datasheet.  The Miscellaneous_Notes field is NOT a section on the
    datasheet.  This field contains the following types of information: 1)
    Remarks written on the datasheet that were not written in a particular
    section, For example, stray remarks written in margins of the datasheet,
    or references to species codes: "Ap = Apc" or "Gr2= At2 and Bh2", or
    "Cpo = Ceanothus prostrates."  2) Observations about the condition of
    the datasheet.  For ex., if the datasheet was torn, if the datasheet is
    blank, or if the datasheet has additional information attached to it
    such as a grass plot datasheet for the same plot.  3) Other potentially
    important observations about the datasheet.  For ex., if the datasheet
    looks like it may contain resurvey data, or if some data was crossed out
    and changed to something else in a different color pencil or pen.  4)
    This field also served as a holding place for data that did not fit the
    format requirements of the database fields.




plotdata-trees

  Tree and shrub vegetation data.  Each row refers to one species found in the 
  plot.
  
  *Fields*

  PID                                     
    Foreign key, referenced PLOT.PID

  PLOTKEY                                 
    Foreign key, referenced PLOT.PLOTKEY.  Combination of map number and
    plot number, without spaces or dashes.

  TREE_ID                                 
    Primary key.

  TREE_SPECIES                            
    Species code as written on the datasheet.

  DIAM_CLASS_4_11                         
    Diameter class (inches): number of stems found between 4 in. and 11 in.,
    as written on the datasheet.

  DIAM_CLASS_12_23                        
    Diameter class (inches): number of stems found between 12 in. and 23
    in., as written on the datasheet.

  DIAM_CLASS_24_35                        
    Diameter class (inches): number of stems found between 24 in. and 35
    in., as written on the datasheet.

  DIAM_CLASS_36_                          
    Diameter class (inches): number of stems found greater than 35 in., as
    written on the datasheet.

  TOTAL                                   
    Total stems as written on datasheet.  This field was later converted to
    a calculated field that was the sum of dbh counts recorded on the
    datasheet.  The original version of this field (ie non-calculated) was
    archived in case it was wanted in the future.                           
                                                                            
                                            

  HT_FEET                                 
    Average height in feet of all trees of this species as written on the
    datasheet.


  genus
    Probable genus for this code.
    
  species
    Probable specific epithet for this code.
    
  var_subsp
    Probable variety or subspecies for this code.
    
  source
    The source of the code-to-name translation (See 
    http://vtm.berkeley.edu/about/faq.php#4)
    
  code_match
    Whether the code was uniquely matched to a single species, or whether its 
    translation is ambiguous.
    
  name
    Full translated name of the species, including multiple names separated by 
    " OR " for ambiguous codes.
    
  unique_matches
    The number of unique code-to-name translations found for this code.


plotdata-brush

  Brush and herbaceous vegetation data.  Each row refers to one species found in 
  the plot.
  
  *Fields*

  PID                                     
    Foreign key, referenced PLOT.PID

  PLOTKEY                                 
    Foreign key, referenced PLOT.PLOTKEY.  Combination of map number and
    plot number, without spaces or dashes.

  COVER_ID                                
    Primary key.

  BRUSH_SPECIES                           
    Species code as written on the datasheet.

  PERCENT                                 
    Percent cover as written on the datasheet.

  HEIGHT                                  
    Plant height in feet as written on the datasheet.

  LITTER_DEPTH                            
    Depth of species litter in inches as written on datasheet.


  genus
    Probable genus for this code.
    
  species
    Probable specific epithet for this code.
    
  var_subsp
    Probable variety or subspecies for this code.
    
  source
    The source of the code-to-name translation (See 
    http://vtm.berkeley.edu/about/faq.php#4)
    
  code_match
    Whether the code was uniquely matched to a single species, or whether its 
    translation is ambiguous.
    
  name
    Full translated name of the species, including multiple names separated by 
    " OR " for ambiguous codes.
    
  unique_matches
    The number of unique code-to-name translations found for this code.
    

plotdata-flatTrees & plotdata-flatBrush

  These files are flattened, non-relational views of the plot data.  They 
  contain all the data in the -plot file plus all the species found in that plot 
  on a single row.
  
  *Additional Fields*
  
  sp_code
    Species code as written on the datasheet.
  
  sp_name
    Probable species name (See http://vtm.berkeley.edu/about/faq.php)
  
  sp_name_source
    The source of code-to-name translation (See 
    http://vtm.berkeley.edu/about/faq.php)

