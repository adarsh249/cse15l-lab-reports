## Lab Report 3

### grep -w Examples

The grep command normally searches the string you entered through all the files, even if it is a substring of a word. For example, if you wrote `grep "app" <path>"` then grep could return a string such as "apple", since "app" is in "apple". With the -w command line option, grep will only match the exact word if it finds it, not substrings.

``` 
adarshpatel@Adarshs-MacBook-Air docsearch % grep -w "exile" technical/*/*.txt
technical/911report/chapter-1.txt:    He was, and is, right. But the conflict did not begin on 9/11. It had been publicly declared years earlier, most notably in a declaration faxed early in 1998 to an Arabic-language newspaper in London. Few Americans had noticed it. The fax had been sent from thousands of miles away by the followers of a Saudi exile gathered in one of the most remote and impoverished countries on earth.
technical/911report/chapter-13.3.txt:            85. For aid to the exile groups, see Karl Inderfurth interview (Feb. 18, 2004); Peter
technical/911report/chapter-2.txt:            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
technical/911report/chapter-2.txt:                for peaceful opposition, forcing their critics to choose silence, exile, or violent
technical/911report/chapter-2.txt:                many into exile. In Pakistan, a military regime sought to justify its seizure of
technical/911report/chapter-3.txt:            Another diplomatic option may have been available: nurturing Afghan exile groups as a
technical/911report/chapter-3.txt:                provided some support for talks among the leaders of exile Afghan groups, including
technical/911report/chapter-3.txt:                told us that the exile groups were not ready to move forward and that coordinating
```
In this case, our command is matching the string "exile" to any of the files that follow the pattern /technical/*/*.txt which also include the string "exile" exactly. This can be useful if you are trying to find a certain word in a number of files. It's similar to using "Ctrl + F" on a webpage, but just to find the exact string, not a substring.

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -w "adults" technical/*/1468-6708-3-1.txt
        Older adults are frequently counseled to lose weight,
        non-smoking older adults have investigated the association
        adults drew similar conclusions [ 7 ] .
        Many healthy older adults report gradual weight gain
        In older adults, risk factors may have a greater effect
        years of being healthy, in a cohort of older adults for
        modification interventions in older adults.
          population-based longitudinal study of 5,888 adults aged
          categories could be combined for older adults. Since
          interventions for older adults who were merely overweight
          adults are the subjects. This is particularly important
          33 34 ] . For older adults, the risks associated with
          outcome for a trial of weight loss in older adults
          found for underweight older adults. Clinical trials whose
        older adults, especially for women. Future efforts to
        no excess risk for older adults who would be classified as
        obese or underweight older adults, and discouraging trials
        that address older adults who are merely overweight.
```
Here, we grep the string "adults" in just one file, and the command returns each line that has the string "adults" in it. Similar to the pervious one, the command will just return the line that includes the given string. Again, this is similar to a doing "Ctrl + F" on a webpage.

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -w "Superman" technical/*/*.txt    
adarshpatel@Adarshs-MacBook-Air docsearch % 
```
In this case, we grepped for the string "Superman" and the command returned nothing, meaning that "Superman" does not exist in any of the files that follow the given pattern.

Another command line option includes -l in which grep will only display the filenames after searching for the given string.

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -l "medical" technical/*/*.txt
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-9.txt
technical/biomed/1468-6708-3-10.txt
technical/biomed/1468-6708-3-4.txt
technical/biomed/1471-2091-4-1.txt
technical/biomed/1471-2105-3-16.txt
technical/biomed/1471-2105-3-17.txt
technical/biomed/1471-2105-3-28.txt
technical/biomed/1471-213X-1-11.txt
technical/biomed/1471-2148-2-7.txt
technical/biomed/1471-2156-2-17.txt
technical/biomed/1471-2156-2-7.txt
technical/biomed/1471-2156-3-3.txt
technical/biomed/1471-2164-3-19.txt
technical/biomed/1471-2164-3-7.txt
technical/biomed/1471-2172-2-10.txt
technical/biomed/1471-2172-3-4.txt
technical/biomed/1471-2180-2-7.txt
technical/biomed/1471-2210-2-9.txt
technical/biomed/1471-2210-3-1.txt
technical/biomed/1471-2261-1-6.txt
technical/biomed/1471-2288-1-9.txt
technical/biomed/1471-2288-2-4.txt
technical/biomed/1471-2296-3-18.txt
technical/biomed/1471-2296-3-19.txt
technical/biomed/1471-230X-1-6.txt
technical/biomed/1471-2318-3-2.txt
technical/biomed/1471-2334-1-10.txt
technical/biomed/1471-2334-1-9.txt
technical/biomed/1471-2334-2-1.txt
technical/biomed/1471-2334-2-24.txt
technical/biomed/1471-2334-2-29.txt
technical/biomed/1471-2334-3-10.txt
technical/biomed/1471-2334-3-11.txt
technical/biomed/1471-2350-2-8.txt
technical/biomed/1471-2350-3-1.txt
technical/biomed/1471-2350-3-7.txt
technical/biomed/1471-2350-3-9.txt
technical/biomed/1471-2350-4-3.txt
technical/biomed/1471-2369-3-1.txt
technical/biomed/1471-2369-3-10.txt
technical/biomed/1471-2369-3-9.txt
technical/biomed/1471-2369-4-1.txt
technical/biomed/1471-2377-3-4.txt
technical/biomed/1471-2407-1-13.txt
technical/biomed/1471-2407-2-3.txt
technical/biomed/1471-2407-2-31.txt
technical/biomed/1471-2407-3-14.txt
technical/biomed/1471-2407-3-18.txt
technical/biomed/1471-2407-3-5.txt
technical/biomed/1471-2415-3-1.txt
technical/biomed/1471-2431-2-11.txt
technical/biomed/1471-2431-3-4.txt
technical/biomed/1471-244X-2-9.txt
technical/biomed/1471-2458-1-9.txt
technical/biomed/1471-2458-2-11.txt
technical/biomed/1471-2458-2-16.txt
technical/biomed/1471-2458-2-18.txt
technical/biomed/1471-2458-2-21.txt
technical/biomed/1471-2458-2-25.txt
technical/biomed/1471-2458-2-3.txt
technical/biomed/1471-2458-2-6.txt
technical/biomed/1471-2458-3-11.txt
technical/biomed/1471-2458-3-20.txt
technical/biomed/1471-2458-3-9.txt
technical/biomed/1471-2466-1-1.txt
technical/biomed/1471-2466-2-4.txt
technical/biomed/1471-2466-3-1.txt
technical/biomed/1471-2474-2-1.txt
technical/biomed/1471-2490-3-2.txt
technical/biomed/1471-5945-1-3.txt
technical/biomed/1472-6793-2-8.txt
technical/biomed/1472-6793-3-5.txt
technical/biomed/1472-6807-1-1.txt
technical/biomed/1472-6815-2-3.txt
technical/biomed/1472-6823-3-1.txt
technical/biomed/1472-6831-2-2.txt
technical/biomed/1472-684X-1-5.txt
technical/biomed/1472-684X-2-1.txt
technical/biomed/1472-684X-2-2.txt
technical/biomed/1472-6874-2-1.txt
technical/biomed/1472-6874-2-13.txt
technical/biomed/1472-6874-3-2.txt
technical/biomed/1472-6882-1-11.txt
technical/biomed/1472-6882-1-12.txt
technical/biomed/1472-6882-1-7.txt
technical/biomed/1472-6882-3-1.txt
technical/biomed/1472-6882-3-3.txt
technical/biomed/1472-6904-1-2.txt
technical/biomed/1472-6920-1-3.txt
technical/biomed/1472-6920-2-1.txt
technical/biomed/1472-6920-2-3.txt
technical/biomed/1472-6947-1-5.txt
technical/biomed/1472-6947-1-6.txt
technical/biomed/1472-6947-2-4.txt
technical/biomed/1472-6947-2-7.txt
technical/biomed/1472-6947-3-5.txt
technical/biomed/1472-6947-3-8.txt
technical/biomed/1472-6955-2-1.txt
technical/biomed/1472-6963-1-11.txt
technical/biomed/1472-6963-1-8.txt
technical/biomed/1472-6963-2-10.txt
technical/biomed/1472-6963-3-1.txt
technical/biomed/1472-6963-3-11.txt
technical/biomed/1472-6963-3-12.txt
technical/biomed/1472-6963-3-13.txt
technical/biomed/1472-6963-3-14.txt
technical/biomed/1472-6963-3-6.txt
technical/biomed/1472-6963-3-7.txt
technical/biomed/1475-2832-1-1.txt
technical/biomed/1475-2891-2-1.txt
technical/biomed/1475-925X-2-12.txt
technical/biomed/1475-9276-1-3.txt
technical/biomed/1476-069X-2-2.txt
technical/biomed/1476-069X-2-7.txt
technical/biomed/1476-069X-2-9.txt
technical/biomed/1476-0711-2-3.txt
technical/biomed/1476-0711-2-7.txt
technical/biomed/1476-4598-2-24.txt
technical/biomed/1477-7525-1-12.txt
technical/biomed/1477-7525-1-9.txt
technical/biomed/1477-7827-1-27.txt
technical/biomed/1477-7827-1-54.txt
technical/biomed/1478-7954-1-3.txt
technical/biomed/ar309.txt
technical/biomed/ar387.txt
technical/biomed/ar750.txt
technical/biomed/bcr45.txt
technical/biomed/bcr570.txt
technical/biomed/bcr583.txt
technical/biomed/bcr618.txt
technical/biomed/cc1044.txt
technical/biomed/cc105.txt
technical/biomed/cc1477.txt
technical/biomed/cc1495.txt
technical/biomed/cc1497.txt
technical/biomed/cc1498.txt
technical/biomed/cc1529.txt
technical/biomed/cc1538.txt
technical/biomed/cc1547.txt
technical/biomed/cc1843.txt
technical/biomed/cc2171.txt
technical/biomed/cc2190.txt
technical/biomed/cc3.txt
technical/biomed/cc303.txt
technical/biomed/cc343.txt
technical/biomed/cc367.txt
technical/biomed/cc4.txt
technical/biomed/cc713.txt
technical/biomed/cc973.txt
technical/biomed/cvm-2-1-038.txt
technical/biomed/cvm-2-4-180.txt
technical/biomed/cvm-2-6-286.txt
technical/biomed/gb-2001-2-4-research0012.txt
technical/biomed/gb-2002-3-10-research0055.txt
technical/biomed/gb-2003-4-3-r20.txt
technical/biomed/gb-2003-4-4-r28.txt
technical/biomed/gb-2003-4-7-r46.txt
technical/biomed/rr191.txt
technical/biomed/rr37.txt
technical/biomed/rr73.txt
technical/plos/journal.pbio.0020001.txt
technical/plos/journal.pbio.0020047.txt
technical/plos/journal.pbio.0020053.txt
technical/plos/journal.pbio.0020063.txt
technical/plos/journal.pbio.0020116.txt
technical/plos/journal.pbio.0020150.txt
technical/plos/journal.pbio.0020156.txt
technical/plos/journal.pbio.0020187.txt
technical/plos/journal.pbio.0020228.txt
technical/plos/journal.pbio.0020276.txt
technical/plos/journal.pbio.0020353.txt
technical/plos/journal.pbio.0020440.txt
technical/plos/journal.pbio.0030097.txt
technical/plos/pmed.0010008.txt
technical/plos/pmed.0010010.txt
technical/plos/pmed.0010013.txt
technical/plos/pmed.0010021.txt
technical/plos/pmed.0010022.txt
technical/plos/pmed.0010034.txt
technical/plos/pmed.0010039.txt
technical/plos/pmed.0010042.txt
technical/plos/pmed.0010046.txt
technical/plos/pmed.0010052.txt
technical/plos/pmed.0010056.txt
technical/plos/pmed.0020009.txt
technical/plos/pmed.0020034.txt
technical/plos/pmed.0020040.txt
technical/plos/pmed.0020055.txt
technical/plos/pmed.0020059.txt
technical/plos/pmed.0020060.txt
technical/plos/pmed.0020062.txt
technical/plos/pmed.0020067.txt
technical/plos/pmed.0020068.txt
technical/plos/pmed.0020071.txt
technical/plos/pmed.0020088.txt
technical/plos/pmed.0020090.txt
technical/plos/pmed.0020098.txt
technical/plos/pmed.0020099.txt
technical/plos/pmed.0020102.txt
technical/plos/pmed.0020118.txt
technical/plos/pmed.0020123.txt
technical/plos/pmed.0020149.txt
technical/plos/pmed.0020158.txt
technical/plos/pmed.0020181.txt
technical/plos/pmed.0020182.txt
technical/plos/pmed.0020187.txt
technical/plos/pmed.0020191.txt
technical/plos/pmed.0020196.txt
technical/plos/pmed.0020203.txt
technical/plos/pmed.0020206.txt
technical/plos/pmed.0020208.txt
technical/plos/pmed.0020209.txt
technical/plos/pmed.0020210.txt
technical/plos/pmed.0020212.txt
technical/plos/pmed.0020226.txt
technical/plos/pmed.0020232.txt
technical/plos/pmed.0020246.txt
technical/plos/pmed.0020247.txt
technical/plos/pmed.0020249.txt
technical/plos/pmed.0020278.txt
```
In this case, we searched for the string "medical" in the techincal/*/*.txt pattern and the command using -l only returned the file paths. This is useful since our terminal would get filled if grep went out and printed the lines of each of these files. 

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -l "weather" technical/*/*.txt
technical/911report/chapter-1.txt
technical/911report/chapter-6.txt
technical/biomed/1471-213X-1-6.txt
technical/biomed/1471-2148-2-2.txt
technical/biomed/1471-2458-2-11.txt
technical/biomed/1472-6785-1-5.txt
technical/biomed/1472-6785-2-7.txt
technical/biomed/1476-0711-2-7.txt
technical/biomed/1476-072X-2-4.txt
technical/plos/journal.pbio.0020054.txt
technical/plos/journal.pbio.0020216.txt
technical/plos/pmed.0020144.txt
technical/plos/pmed.0020272.txt
```
Here is another example where we want to find files with "weather" but only want it to return the path and file names. Another reason this is useful is if one file has the string "weather" multiple times, instead of grep printing each line with weather in the file, it will just tell you the file, again, not overcrowding our terminal. 

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -l "Carry" technical/*/*.txt
technical/biomed/1476-0711-2-7.txt
```
One last example that only returned one file. Obviously in this case, we don't know what files have which words, but when the output is small like this, it would be useful to see the line including "Carry" here so we wouldn't have to click on the file to find out where it is in the file. This could be one downside to using the -l option.

Another cool command line argument includes -r, which will recursivley go through every file in a given directory and search it. (If you noticed earlier, the pattern didn't actually get every directory with .txt files)

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -r "Canada" technical
technical/government/About_LSC/Progress_report.txt:Wales, Canada and the United States along with Germany and the
technical/government/About_LSC/Strategic_report.txt:Aid Group and through the Ontario (Canada) Legal Aid Speakers
technical/government/About_LSC/Strategic_report.txt:o Ontario Legal Aid Speakers Series (Canada)
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:How does this relate to Canada and, specifically, the initiative
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:services system? Legal services programs in Canada are about the
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:Here in Canada. And in the United States.
technical/government/Env_Prot_Agen/multi102902.txt:Canada. These numbers are up from the 1990's when a severe drought
technical/government/Env_Prot_Agen/ctf1-6.txt:only 1 out of 100 tests (Environment Canada, 1990). When a result
technical/government/Env_Prot_Agen/ro_clear_skies_book.txt:Energy Economics, Quebec City, Canada, May 1998.
technical/government/Env_Prot_Agen/ctm4-10.txt:only 1 out of 100 tests (Environment Canada, 1990). When a result
technical/government/Env_Prot_Agen/atx1-6.txt:(Environment Canada, 1990). When a result from a reference toxicant
technical/government/Gen_Account_Office/d0269g.txt:programs in both the United States and Canada.
technical/government/Gen_Account_Office/d01376g.txt:Chief Information Officer ¬ Treasury Board of Canada:
technical/government/Gen_Account_Office/pe1019.txt:Educational Research Association meeting, Toronto, Canada, April
technical/government/Gen_Account_Office/pe1019.txt:Educational Research Association meeting, Montreal, Canada, April,
technical/government/Gen_Account_Office/gg96118.txt:as Australia, Canada, New Zealand, and the United Kingdom. Many of
technical/government/Gen_Account_Office/gg96118.txt:international trade agreements, such as the U.S.-Canada Free Trade
technical/government/Gen_Account_Office/gg96118.txt:Canada, on the other hand, hold their program managers accountable
technical/government/Gen_Account_Office/d01591sp.txt:0 Japan Italy France Germany Canada United United Kingdom States
technical/government/Gen_Account_Office/d01591sp.txt:G-7 nations-Canada, France, Germany, Italy,
technical/government/Gen_Account_Office/Oct15-2001_d0224.txt:the entire United States and Canada and a small part of Mexico.
technical/government/Gen_Account_Office/ai00134.txt:Treasury Board of Canada Secretariat- www.tbssct.gc.ca
technical/government/Gen_Account_Office/ai00134.txt:associated with Canada's initiative to modernize its
technical/government/Gen_Account_Office/ai9868.txt:Canada rely on
technical/government/Gen_Account_Office/May1998_ai98068.txt:Canada rely on
technical/government/Post_Rate_Comm/Mitchell_RMVancouver.txt:University, Vancouver, Canada, June 710, 2000 2 The writer is
technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt:sample (Canada, Finland, and Portugal deliver five times per week,
technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt:Canada Post, Consignia (Royal Mail), Posti Finland and La Poste
technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt:unit costs and adjusted only for deliveries per week (Canada,
technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt:Canada 43 41 Finland 34 39 France 38b 40b Germany 50 57 Italy 90
technical/government/Post_Rate_Comm/Redacted_Study.txt:(excluding Canada). This result is valid to the extent that the
technical/government/Post_Rate_Comm/Redacted_Study.txt:volume of mail exchanged between the U.S. Postal Service and Canada
technical/government/Post_Rate_Comm/Redacted_Study.txt:rates with Canada, and Canada is the largest market for U.S.
technical/government/Post_Rate_Comm/Redacted_Study.txt:mail, excluding outbound rates to Canada, by 7.5 percent.
technical/government/Post_Rate_Comm/Redacted_Study.txt:except for Canada and Mexico, it was not possible to develop a
technical/government/Post_Rate_Comm/Redacted_Study.txt:excluding Canada, was a reasonable proxy for the weight interval
technical/government/Post_Rate_Comm/Cohenetal_comparison.txt:countries, Canada, New Zealand and Australia, the effect on unit
technical/government/Media/Few_who_need.txt:England, Canada, Australia, Scotland and New Zealand spend anywhere
technical/government/Media/Assuring_Underprivileged.txt:According to Deputy Public Defender Debbie Canada, jurors also
technical/government/Media/Assuring_Underprivileged.txt:"She's very good with juries," Canada said. "She's very polite,
technical/plos/pmed.0020113.txt:        In Canada, hypertension is the leading primary diagnosis for patient visits to physicians'
technical/plos/pmed.0020113.txt:        Canada, accounting for 20% of prescription drug sales.
technical/plos/pmed.0020274.txt:        with the virus found in Australia, Canada, Japan, Belgium, and the US. Thus, health
technical/plos/pmed.0020115.txt:        in Canada, the Edmonton protocol, uses ß-cells isolated from human cadavers and has shown
technical/plos/journal.pbio.0020054.txt:        in"journal" Canada (Figure 1). And they can take preemptive measures, such as reducing fuel
technical/plos/journal.pbio.0020054.txt:        The tool is a variation of the Fire Danger Rating System used in Canada and, with
technical/plos/journal.pbio.0020054.txt:        Brady doesn't expect immediate results in terms of reducing acreage burned. “Canada and
technical/plos/journal.pbio.0020121.txt:        States and Canada are the only countries in which it has been identified, apart from a few
technical/plos/pmed.0010064.txt:          using the TruGene Assay (Visible Genetics, Toronto, Canada) at the Gladstone Institute of
technical/plos/journal.pbio.0030056.txt:        says Michael Bunce, an anthropologist at MacMaster University in Ontario, Canada. Analysis
technical/plos/journal.pbio.0020113.txt:        (Halifax, Nova Scotia, Canada). And that is where fisheries have adequate access to current
technical/plos/journal.pbio.0020113.txt:        Canada's endangered species list (Figure 1). From 2 billion breeding individuals in the
technical/plos/journal.pbio.0020113.txt:        Columbia, Canada), has shown that increased fishing has caused the industry to “fish down
technical/plos/journal.pbio.0020112.txt:        countries, Japan, Canada, and the United States.
technical/plos/journal.pbio.0020306.txt:        Canada, somewhat accidentally laid the foundations of ‘diatom nanotechnology’ in 1988 when
technical/plos/journal.pbio.0020001.txt:        lion's share (84.2%), followed by Canada (10.35%). Latin America as a whole contributed
technical/plos/journal.pbio.0020001.txt:        most rapidly in the Americas, far outpacing the United States and Canada (Figure 1).
technical/plos/journal.pbio.0020001.txt:        Canada and United States, the trend in Latin America has been an increase in relative
technical/plos/journal.pbio.0020001.txt:        States and Canada by the year 2000 (Figure 2). Although the cost of research is undoubtedly
technical/plos/journal.pbio.0020001.txt:        effort compared with that of the United States (2.84%) and Canada (1.5%).
technical/plos/journal.pbio.0020001.txt:        United States (1.5) and even Canada (3.3) (RICYT 2002). Other countries, such as Costa
technical/plos/journal.pbio.0020001.txt:            Canada?
technical/plos/journal.pbio.0020001.txt:        Latin America compared with the relatively flat increases in the United States and Canada,
technical/plos/journal.pbio.0020001.txt:        United States and Canada. This pattern could be the result of a variety of factors, none of
technical/plos/journal.pbio.0020001.txt:        the decreasing trends in the number of publications per investment dollar in Canada and
technical/plos/journal.pbio.0020001.txt:        however, Latin America represented only 6%, while Canada and United States accounted,
technical/plos/journal.pbio.0020001.txt:        Canada across all subject areas in 
technical/plos/journal.pbio.0020001.txt:        versus 6% in the top 20 ecological journals, whereas the United States and Canada had 81%
technical/biomed/1471-2091-2-11.txt:          Life Technologies (Burlington, ON, Canada). [
technical/biomed/1471-2091-2-11.txt:          Canada). Bile acids were obtained from Sigma-Aldrich
technical/biomed/1471-2091-2-11.txt:          Canada Ltd. (Oakville, ON, Canada) and
technical/biomed/1471-2091-2-11.txt:          protease inhibitor cocktail (Sigma-Aldrich Canada Ltd.).
technical/biomed/1468-6708-3-10.txt:        Canada, Puerto Rico and the US Virgin Islands.
technical/biomed/1476-0711-2-7.txt:        In Canada a route conversion program on the prescribing
technical/biomed/1471-2180-2-35.txt:        Canada; Exponential Biotherapies Inc. of Port Washington,
technical/biomed/1477-7827-1-17.txt:          Canada), sFasL (50 ng/ml; Oncogene, LaJolla, CA), mouse
technical/biomed/1471-2350-4-6.txt:        centers in the U.S. and Canada, were screened by TCD [ 10 ]
technical/biomed/rr167.txt:          patients with CF in Vancouver, Canada, kindly provided by
technical/biomed/bcr631.txt:          Fitall (MTR software, Toronto, Canada) modified with an
technical/biomed/1472-6785-1-5.txt:        across the boreal forest of Canada, is generally two or
technical/biomed/1472-6890-1-4.txt:          ethanol, cleared in xylene and mounted in Canada balsam.
technical/biomed/1471-2164-3-16.txt:          Research, Inc., St. Catherine's, Ontario, Canada), and
technical/biomed/1472-6920-2-3.txt:        Academic Medicine. These countries are the USA, Canada and
technical/biomed/1472-6920-2-3.txt:        Australia, Canada, Hong Kong, New Zealand, Sweden, the
technical/biomed/1472-6920-2-3.txt:        their colleagues from Canada for 7.2% of all articles in
technical/biomed/1472-6920-2-3.txt:        authors from the United Kingdom, Australia, the USA, Canada
technical/biomed/1472-6920-2-3.txt:        Australia, Canada and the USA were the main contributors to
technical/biomed/1471-2350-3-1.txt:            participating centers in the United States and Canada
technical/biomed/1472-6882-2-5.txt:        the Hospital for Sick Children in Toronto, Ontario, Canada.
technical/biomed/1471-230X-1-10.txt:          (Imaging Research, St. Catherines, Ontario, Canada).
technical/biomed/1477-7827-1-6.txt:          Canada). Mouse monoclonal anti-8-oxoguanine (4355-MC-100)
technical/biomed/1472-6963-3-7.txt:        seventh leading cause of death in Canada with at least
technical/biomed/1472-6963-3-7.txt:        ] . It has been reported that in Canada 21% of patients
technical/biomed/1472-6963-3-7.txt:        Canada, accounting for 32% and 50% of new cases,
technical/biomed/1472-6963-3-7.txt:        Canada has reported that twice as many patients with
technical/biomed/1472-6963-3-7.txt:        In 1993, the economic burden of diabetes to Canada was
technical/biomed/1472-6963-3-7.txt:        reflect the cost of diabetes for Canada. Yet, it is not
technical/biomed/1472-6963-3-7.txt:          , the Heart Disease and Stroke Foundation of Canada [ 22
technical/biomed/1472-6963-3-7.txt:          23 ] , Health Canada [ 23 24 25 ] , Canadian clinical
technical/biomed/1472-6963-3-7.txt:          Reimbursement for health care in Canada is largely
technical/biomed/1472-6963-3-7.txt:          from Statistics Canada [ 42 ] were used to derive a ratio
technical/biomed/1472-6963-3-7.txt:          disposition data from Canada were used in the analysis,
technical/biomed/1472-6963-3-7.txt:          Statistics Canada [ 42 ] .
technical/biomed/1472-6963-3-7.txt:        problems for Canada. Nearly 6% of the Canadian population
technical/biomed/1472-6963-3-7.txt:        complications in Canada given the data available at the
technical/biomed/1472-6963-3-7.txt:        estimate for Canada.
technical/biomed/1472-6963-3-7.txt:        treated in the hospital initially in Canada. If the TIA
technical/biomed/1472-6963-3-7.txt:        diabetes in Canada could not be identified. While a study
technical/biomed/1472-6963-3-7.txt:        health care decision makers in Canada, who cannot wait for
technical/biomed/1471-2210-2-5.txt:          Research Inc., Ontario, Canada). All immunochemical
technical/biomed/1472-6963-3-12.txt:        health care systems such as those in Canada and Europe. The
technical/biomed/1472-6963-3-12.txt:        rate for CABS in Ontario, Canada, was only 67.4 per
technical/biomed/1472-6963-3-12.txt:        Canada would be higher if only men were included. A similar
technical/biomed/1472-6963-3-12.txt:        and the province of Ontario in Canada is relevant because
technical/biomed/1472-684X-2-2.txt:        patients released in Canada provide a clear, but certainly
technical/biomed/1471-2350-3-9.txt:        have been reported from Canada, Utah, and Minnesota [ 17 18
technical/biomed/1472-6750-3-4.txt:          (Ad5.CMV-LacZ) (Qbiogene, Montreal, Canada). The
technical/biomed/1471-2121-3-25.txt:          Victoria, BC, Canada), anti-GFP (Clontech, Inc. Palo
technical/biomed/1471-2210-1-7.txt:          from Baxter Healthcare Corp. (Toronto, ONT, Canada) and
technical/biomed/1471-2458-3-11.txt:        mid-1980s in Canada where 52% of the cases of
technical/biomed/1477-7827-1-31.txt:          by B.R. Downey (McGill University, Montreal, Canada).
technical/biomed/1471-230X-2-17.txt:        grant from Janssen Ortho Canada.
technical/biomed/1476-4598-1-6.txt:          Research, Inc., St. Catharines, Ontario, Canada), and the
technical/911report/chapter-13.4.txt:                broker and an illegal alien in Canada from Cameroon who failed to surrender himself
technical/911report/chapter-13.5.txt:                by the summer of 2001 while in Canada. FBI briefing (June 24, 2004); Intelligence
technical/911report/chapter-13.5.txt:                regime, such as now exists for travel to the United States from Canada and Ireland.
technical/911report/chapter-13.2.txt:                United States and Canada. According to the agreement in effect on 9/11, the "primary
technical/911report/chapter-13.2.txt:                "providing surveillance and control of the airspace of Canada and the United
technical/911report/chapter-13.2.txt:                States." See DOS memo, Exchange of Notes Between Canada and the United States
technical/911report/chapter-13.3.txt:                entering the United States via Canada, see, e.g., INS record, Record of Deportable
technical/911report/chapter-3.txt:                Canada had one agent for every 13.25 miles. Despite examples of terrorists entering
technical/911report/chapter-3.txt:                from Canada, awareness of terrorist activity in Canada and its more lenient
technical/911report/chapter-1.txt:NORAD Mission and Structure. NORAD is a binational command established in 1958 between the United States and Canada. Its mission was, and is, to defend the airspace of North America and protect the continent. That mission does not distinguish between internal and external threats; but because NORAD was created to counter the Soviet threat, it came to define its job as defending against external attacks.
technical/911report/chapter-6.txt:            Ahmed Ressam, 23, had illegally immigrated to Canada in 1994. Using a falsified
technical/911report/chapter-6.txt:                $12,000. Back in Canada, he went about procuring weapons, chemicals, and false
technical/911report/chapter-6.txt:                travel documents to enter Canada, Ressam decided to carry out the plan alone. By the
technical/911report/chapter-6.txt:                Canada, to Port Angeles, Washington. Ressam planned to drive to Seattle and meet
technical/911report/chapter-6.txt:                and then return to Canada. Impressed, Abu Zubaydah asked Ressam to get more genuine
technical/911report/chapter-6.txt:                controls on the Canadian border (including stepping up U.S.-Canada cooperation). The
technical/911report/chapter-6.txt:                undertaking a Joint Perimeter Defense program with Canada to establish
technical/911report/chapter-8.txt:                cell in Canada that an anonymous caller had claimed might be planning an attack
technical/911report/chapter-8.txt:                The millennium plotting in Canada in 1999 may have been part of Bin Ladin's first
technical/911report/chapter-12.txt:                    carrying passports when returning from Canada, Mexico, and the Caribbean. The
technical/911report/chapter-12.txt:                entrances between our ports of entry, working with Canada and Mexico as much as
```
In this case, we recursively searched for the string "Canada" and we got files from the technical/government directory which we were not getting before. This can be useful for a file system that has multiple files in many different directories. 

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -r "grantees" technical
technical/government/About_LSC/LegalServCorp_v_VelazquezSyllabus.txt:lawyers employed by LSC grantees, together with others- filed suit
technical/government/About_LSC/Progress_report.txt:demand. Our grantees now estimate that they currently turn away
technical/government/About_LSC/Progress_report.txt:LSC and our grantees live and work in a world that is marked by
technical/government/About_LSC/Progress_report.txt:This report demonstrates that our grantees and the broader equal
technical/government/About_LSC/Progress_report.txt:with the help and assistance of our grantees. We did it with the
technical/government/About_LSC/Progress_report.txt:grantees and for the clients we are so privileged to serve.
technical/government/About_LSC/Progress_report.txt:Working with grantees in each state to develop systems and
technical/government/About_LSC/Progress_report.txt:Working with grantees and planners in each state to promote
technical/government/About_LSC/Progress_report.txt:grantees, such as bar associations, non-LSC funded legal services
technical/government/About_LSC/Progress_report.txt:LSC has scheduled a meeting with its statewide grantees
technical/government/About_LSC/Progress_report.txt:to technology grantees at no cost to grantees.
technical/government/About_LSC/Progress_report.txt:this year's grantees to the national support system that LSC has
technical/government/About_LSC/Progress_report.txt:developed, with the assistance of numerous grantees. These five
technical/government/About_LSC/Progress_report.txt:national support grants will give our grantees more resources than
technical/government/About_LSC/Progress_report.txt:available to all LSC grantees, not just TIG recipients.
technical/government/About_LSC/Progress_report.txt:closely with NTAP so that grantees with questions can log onto the
technical/government/About_LSC/Progress_report.txt:in Houston. Using WebEx hosting services, our grantees will be able
technical/government/About_LSC/Progress_report.txt:Society of Cincinnati, will help grantees with project evaluations.
technical/government/About_LSC/Progress_report.txt:Building on work undertaken by last year's grantees, LSC has
technical/government/About_LSC/Progress_report.txt:"circuit riders" to assist grantees with content management and to
technical/government/About_LSC/Progress_report.txt:the Legal Aid Society of Orange County will help grantees with
technical/government/About_LSC/Progress_report.txt:Commitment: Working with grantees, LSC has developed and
technical/government/About_LSC/Progress_report.txt:personnel are frequently asked by grantees for assistance with
technical/government/About_LSC/Progress_report.txt:ensuring that grantees have effective administrative systems in
technical/government/About_LSC/Progress_report.txt:performance standards applicable to LSC grantees, and LSC's
technical/government/About_LSC/Progress_report.txt:discussions on the application process with interested grantees and
technical/government/About_LSC/Progress_report.txt:annually by grantees, and report on the diversity trends the
technical/government/About_LSC/Strategic_report.txt:have assisted LSC grantees and state justice communities with this
technical/government/About_LSC/Strategic_report.txt:quality legal services programs. OPP staff work with grantees to
technical/government/About_LSC/Strategic_report.txt:LSC on how best to help grantees reach their diversity goals. The
technical/government/About_LSC/Strategic_report.txt:Using Case Service Reports. CSR's, which grantees are required
technical/government/About_LSC/Strategic_report.txt:grantees' attorney ranks.
technical/government/About_LSC/Strategic_report.txt:grantees. Similarly, OIM revised the electronic Grant Renewal
technical/government/About_LSC/Strategic_report.txt:population for each of our grantees' service areas under these new
technical/government/About_LSC/Strategic_report.txt:figures. This information was supplied to all grantees and will be
technical/government/About_LSC/Strategic_report.txt:Each year, OIM staff assists our grantees in verifying the
technical/government/About_LSC/Strategic_report.txt:grantees a means to ensure that their CSR data meet LSC standards
technical/government/About_LSC/Strategic_report.txt:reveal problems, grantees are asked to consult with LSC to
technical/government/About_LSC/Strategic_report.txt:determine the appropriate corrective action. All grantees are
technical/government/About_LSC/Strategic_report.txt:helps grantees meet critical training needs. In 2002, we designed
technical/government/About_LSC/Strategic_report.txt:volume of our grantees' work and to evaluate the success of their
technical/government/About_LSC/Strategic_report.txt:in the types and numbers of cases closed by grantees. Their
technical/government/About_LSC/Strategic_report.txt:demonstrating that LSC grantees continue to vigorously represent
technical/government/About_LSC/Strategic_report.txt:illustrated what we do not know about our grantees' work - the
technical/government/About_LSC/Strategic_report.txt:million people received significant matters services from grantees
technical/government/About_LSC/Strategic_report.txt:grantees to offer clients services that do not fall into the
technical/government/About_LSC/Strategic_report.txt:LSC grantees and staff, to determine its effectiveness in measuring
technical/government/About_LSC/Strategic_report.txt:system for grantees to both inform the field and create a set of
technical/government/About_LSC/Strategic_report.txt:traveled to meetings with local, regional and state grantees,
technical/government/About_LSC/Strategic_report.txt:represented were our grantees in Puerto Rico, Guam and Virgin
technical/government/About_LSC/Strategic_report.txt:a representative sample of program grantees and technology experts.
technical/government/About_LSC/Strategic_report.txt:areas for improvement, and ways we could encourage grantees to
technical/government/About_LSC/Strategic_report.txt:ensure that grantees' legal work management and supervision is
technical/government/About_LSC/Strategic_report.txt:assist our grantees' staff, when asked; one common request is to
technical/government/About_LSC/Strategic_report.txt:grantees to attract and retain high quality new lawyers. LSC has
technical/government/About_LSC/Strategic_report.txt:Together we have advocated on behalf of LSC grantees at other
technical/government/About_LSC/Strategic_report.txt:the grantees receive.
technical/government/About_LSC/Strategic_report.txt:allocated by Congress to our grantees has ameliorated somewhat the
technical/government/About_LSC/Comments_on_semiannual.txt:269 in 1997, to 167 anticipated grantees (Basic Field and Native
technical/government/About_LSC/Comments_on_semiannual.txt:LSC's ultimate goal in this regard is to help grantees create
technical/government/About_LSC/Comments_on_semiannual.txt:2 'Programs', 'recipients', and 'grantees' are used
technical/government/About_LSC/Comments_on_semiannual.txt:comprehensively improve grantees' delivery of services to
technical/government/About_LSC/Comments_on_semiannual.txt:Grants, it has consulted with grantees on the selection of case
technical/government/About_LSC/Comments_on_semiannual.txt:sub-grantees that receive twenty-five percent (25%) or more of the
technical/government/About_LSC/Comments_on_semiannual.txt:LSC grant award, and sub-grantees that deliver a full range of
technical/government/About_LSC/Comments_on_semiannual.txt:LSC continues to provide technical assistance to grantees in
technical/government/About_LSC/Special_report_to_congress.txt:For 1999, LSC grantees reported closing 1,038,662 million1 civil
technical/government/About_LSC/Special_report_to_congress.txt:the right of grantees to a hearing to contest a funding decision
technical/government/About_LSC/Special_report_to_congress.txt:(CSR) data submitted annually by our grantees.2 LSC is aware that
technical/government/About_LSC/Special_report_to_congress.txt:insufficient attention by grantees to the existing reporting and
technical/government/About_LSC/Special_report_to_congress.txt:any fraud or intentional misrepresentation by any of the grantees
technical/government/About_LSC/Special_report_to_congress.txt:grantees and the case statistical reports submitted by the
technical/government/About_LSC/Special_report_to_congress.txt:grantees' reports on which the measure was based. A series of
technical/government/About_LSC/Special_report_to_congress.txt:accuracy of case statistical reports submitted by six grantees, and
technical/government/About_LSC/Special_report_to_congress.txt:systems and the reconfiguration of grantees accelerated following
technical/government/About_LSC/Special_report_to_congress.txt:closed cases reported by the five grantees in 1997. The percentage
technical/government/About_LSC/Special_report_to_congress.txt:1997 CSR data, which had already been submitted by the grantees,
technical/government/About_LSC/Special_report_to_congress.txt:to heighten the awareness of grantees to the CSR requirements and
technical/government/About_LSC/Special_report_to_congress.txt:reported to Congress, though, a number of grantees did voluntarily
technical/government/About_LSC/Special_report_to_congress.txt:LSC reissued its CSR instructions to all grantees, calling
technical/government/About_LSC/Special_report_to_congress.txt:required all grantees to perform a self-inspection of their CSR
technical/government/About_LSC/Special_report_to_congress.txt:data, has followed up on grantees where corrective action was found
technical/government/About_LSC/Special_report_to_congress.txt:grantees.
technical/government/About_LSC/Special_report_to_congress.txt:For 1999, LSC grantees reported closing 1,038,662 civil legal
technical/government/About_LSC/Special_report_to_congress.txt:7 In 1999, it is estimated that LSC grantees received
technical/government/About_LSC/Special_report_to_congress.txt:reported by LSC grantees (1,038,662) by the average estimated error
technical/government/About_LSC/Special_report_to_congress.txt:represents only a portion of the work conducted by LSC grantees.
technical/government/About_LSC/Special_report_to_congress.txt:8, estimate of cases closed in 1999 by LSC grantees.
technical/government/About_LSC/Special_report_to_congress.txt:some grantees did use Self-Inspection data to exclude
technical/government/About_LSC/Special_report_to_congress.txt:grantees would not have been possible. In six states, the federal
technical/government/About_LSC/Special_report_to_congress.txt:of any particular grantee. LSC strongly encourages all its grantees
technical/government/About_LSC/Special_report_to_congress.txt:considers in evaluating its grantees. LSC believes that the total
technical/government/About_LSC/Special_report_to_congress.txt:number of LSC eligible clients served by LSC grantees is of
technical/government/About_LSC/Special_report_to_congress.txt:funding. Our grantees have successfully leveraged their federal
technical/government/About_LSC/Special_report_to_congress.txt:grantees that can be reasonably attributable to LSC grantees.
technical/government/About_LSC/Special_report_to_congress.txt:system to document and assess the work of LSC grantees. LSC has
technical/government/About_LSC/Special_report_to_congress.txt:implement a pilot project at six LSC grantees that will gather the
technical/government/About_LSC/Special_report_to_congress.txt:captures all the work of LSC grantees, not simply the traditional
technical/government/About_LSC/Special_report_to_congress.txt:2001, LSC will require grantees to provide information that allows
technical/government/About_LSC/Special_report_to_congress.txt:developing and evaluating to assess the work of grantees is a
technical/government/About_LSC/Special_report_to_congress.txt:on-site evaluations of grantees. By comparing the "cost per case"
technical/government/About_LSC/Special_report_to_congress.txt:similarly situated grantees. This measure does require LSC staff to
technical/government/About_LSC/Special_report_to_congress.txt:differences in the types of cases handled by these two grantees, a
technical/government/About_LSC/Special_report_to_congress.txt:surface. Where appropriate, LSC grantees refer low-income persons
technical/government/About_LSC/Special_report_to_congress.txt:of funding source -- being performed by its grantees.
technical/government/About_LSC/Special_report_to_congress.txt:this estimate, total cases reported by LSC grantees would be
technical/government/About_LSC/Special_report_to_congress.txt:grantees to leverage federal dollars using an estimate of cases
technical/government/About_LSC/Special_report_to_congress.txt:LSC routinely evaluates its grantees on their ability to leverage
technical/government/About_LSC/Special_report_to_congress.txt:example, as noted above, grantees often seek alternative funding to
technical/government/About_LSC/Special_report_to_congress.txt:mandates all grantees within a particular state work together to
technical/government/About_LSC/Special_report_to_congress.txt:grantees are required to address how they will work together to
technical/government/About_LSC/Special_report_to_congress.txt:1999, for example, LSC grantees reported closing 1,038,662 civil
technical/government/About_LSC/Special_report_to_congress.txt:reported by LSC grantees (1,038,662) by the average estimated error
technical/government/About_LSC/Special_report_to_congress.txt:conservative, estimate of cases closed in 1999 by LSC grantees.
technical/government/About_LSC/Special_report_to_congress.txt:LSC's grantees annually submit, LSC has committed itself to
technical/government/About_LSC/Special_report_to_congress.txt:to services provided by LSC grantees. Subcommittee Chairman Rep.
technical/government/About_LSC/Special_report_to_congress.txt:statistics provided by LSC to Congress concerning their grantees'
technical/government/About_LSC/CONFIG_STANDARDS.txt:The Legal Services Corporation expects its grantees in each state
technical/government/About_LSC/CONFIG_STANDARDS.txt:level and expects its grantees to do the same.
technical/government/About_LSC/CONFIG_STANDARDS.txt:grantees and encourage DSPB's to critically examine the degree to
technical/government/About_LSC/CONFIG_STANDARDS.txt:which the configuration of LSC grantees in any given state promotes
technical/government/About_LSC/commission_report.txt:services grantees relating to eligible aliens.
technical/government/About_LSC/commission_report.txt:Scope of alien representation. Corporation grantees are
technical/government/About_LSC/commission_report.txt:sole exception of H-2A workers, LSC grantees may provide
technical/government/About_LSC/commission_report.txt:ability to receive legal representation from LSC grantees.
technical/government/About_LSC/commission_report.txt:LSC grantees to provide legal assistance to eligible aliens who
technical/government/About_LSC/commission_report.txt:Corporation when conducting audits of LSC grantees, or from
technical/government/About_LSC/commission_report.txt:grantees, the clients, opposing parties, and the courts. See Part
technical/government/About_LSC/commission_report.txt:status. Under this interpretation, LSC grantees who have begun
technical/government/About_LSC/commission_report.txt:and have not abandoned their residence or INA status. LSC grantees
technical/government/About_LSC/commission_report.txt:their H-2A contract. LSC grantees are authorized to litigate this
technical/government/About_LSC/commission_report.txt:during the course of the representation. LSC grantees may not
technical/government/About_LSC/commission_report.txt:of permissible representation for eligible aliens by LSC grantees.
technical/government/About_LSC/commission_report.txt:LSC grantees are permitted to represent several classes of
technical/government/About_LSC/commission_report.txt:grantees may provide general representation to aliens on all the
technical/government/About_LSC/commission_report.txt:current interpretation used by LSC grantees and the impact of
technical/government/About_LSC/commission_report.txt:categories and H-2A workers: for the former, grantees may represent
technical/government/About_LSC/commission_report.txt:clients by LSC grantees frequently continues for many months. For
technical/government/About_LSC/commission_report.txt:grantees. See April Testimony at 24-25 (testimony of Cynthia Rice,
technical/government/About_LSC/commission_report.txt:represented by LSC-grantees after workers had left the country.
technical/government/About_LSC/commission_report.txt:requirement for representation by LSC grantees. As noted above,
technical/government/About_LSC/commission_report.txt:grantees, the clients, opposing parties, and the courts. An
technical/government/About_LSC/commission_report.txt:status. Under this interpretation, LSC grantees who have begun
technical/government/About_LSC/commission_report.txt:and have not abandoned their residence or INA status. LSC grantees
technical/government/About_LSC/commission_report.txt:their H-2A contract. LSC grantees are authorized to litigate this
technical/government/About_LSC/commission_report.txt:during the course of the representation. LSC grantees may not
technical/government/About_LSC/commission_report.txt:consistent practice of LSC grantees, and the understanding of
technical/government/About_LSC/commission_report.txt:growers, and of Congress. As noted above, LSC grantees have
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:for many grantees.
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:fees. Additional restrictions prevented our grantees from doing
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:told LSC that it could not continue to fund its grantees
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:most difficult part of our strategy to move our grantees into new
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:LSC has asked each of its grantees to undergo a fundamental
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:programs, and a host of others. LSC required its grantees in each
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:grantees worked in isolation within states and across state lines.
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:This was a tremendous change for our grantees and for the delivery
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:work of our grantees in terms of outcomes for clients and projects
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:LSC to cease funding its grantees "presumptively" and to begin to
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:benchmarks exist means that there is a standard that all grantees
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:information on all our grantees against which we can evaluate their
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:legal services program. We have found that many of our grantees
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:grantees, individually and collectively, become the kinds of
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:grantees toward stronger and more aggressive delivery of services
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:become grantees, they are required, as a condition of continued
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:grantees, The penultimate goals is the establishment of
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:Here's the kicker-grantees must do all of this or risk
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:most grantees thought that like many other projects begun by LSC,
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:the "elephant did begin to dance" and LSC, its grantees and the
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:maximize grantees' ability to leverage their federal investment.
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:legal services and cross-program advocacy, and LSC and its grantees
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:Historically, LSC directives were seen by grantees as antithetical
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:failed when we pushed willing, but unprepared grantees to
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:than was necessary by not including willing grantees and other
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:grantees and other stakeholders with some of the planning
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:LSC grantees consist of hundreds of local organizations
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:many instances the grantees are funded by a combination of LSC
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:LSC appropriates funds to grantees or recipients that hire and
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:Amendment rights of LSC grantees and their clients. For purposes of
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:Lawyers employed by New York City LSC grantees, together with
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:grantees, brought suit in the United States District Court for the
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:grantees could not accept representations designed to change
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:three prohibited grantees' involvement in these activities
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:promote a governmental message. Congress funded LSC grantees to
technical/government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:limitation takes into account the nature of the grantees'
technical/government/About_LSC/reporting_system.txt:Starting on July 1, 2001, all LSC grantees began collecting
technical/government/About_LSC/reporting_system.txt:grantees is several times the number of cases being reported on the
technical/government/About_LSC/reporting_system.txt:! More than 75 percent of grantees are providing various forms
technical/government/About_LSC/reporting_system.txt:LSC grantees are playing a significant role in helping courts to
technical/government/About_LSC/reporting_system.txt:! Increasingly, LSC grantees are important gatekeepers, or
technical/government/About_LSC/reporting_system.txt:personal safety. Many LSC grantees operate intake systems that
technical/government/About_LSC/reporting_system.txt:grantees about the range of methods being used by their fellow
technical/government/About_LSC/reporting_system.txt:grantees are contributing to their communities through the
technical/government/About_LSC/reporting_system.txt:services from LSC grantees in the last half of 2001.
technical/government/About_LSC/reporting_system.txt:and follow-up interviews with a sample of grantees. (See Exhibit 1
technical/government/About_LSC/reporting_system.txt:the guidelines provided to grantees, planned for distribution in
technical/government/About_LSC/reporting_system.txt:1. Community legal education. 195 LSC grantees (99.5 percent)
technical/government/About_LSC/reporting_system.txt:grantees, in the second half of 2001, more than 1,450,000 people
technical/government/About_LSC/reporting_system.txt:people visiting web sites maintained by LSC grantees.
technical/government/About_LSC/reporting_system.txt:grantees. It informs low income people about their legal rights and
technical/government/About_LSC/reporting_system.txt:assistance from an attorney. 150 LSC grantees reported that in 2001
technical/government/About_LSC/reporting_system.txt:numbers of grantees providing different types of services were as
technical/government/About_LSC/reporting_system.txt:In the second half of 2001, grantees reported providing
technical/government/About_LSC/reporting_system.txt:4. Outreach. LSC grantees seek to increase visibility in the
technical/government/About_LSC/reporting_system.txt:89 percent of LSC grantees reported that they conducted outreach
technical/government/About_LSC/reporting_system.txt:grantees) was referral agreements with other agencies. These are
technical/government/About_LSC/reporting_system.txt:violence shelters, to refer eligible clients to our grantees. This
technical/government/About_LSC/reporting_system.txt:Increasingly, grantees are using targeted outreach methods
technical/government/About_LSC/reporting_system.txt:they have a legal problem. One hundred sixty nine grantees reported
technical/government/About_LSC/reporting_system.txt:of newer kinds of services that grantees reported as "matters" in
technical/government/About_LSC/reporting_system.txt:It is clear from the Matters Service Reports that LSC grantees
technical/government/About_LSC/reporting_system.txt:clients. It is impractical to restrict grantees to counting only
technical/government/About_LSC/reporting_system.txt:grantees go to considerable lengths to focus services on the
technical/government/About_LSC/reporting_system.txt:provided by grantees. These include
technical/government/About_LSC/reporting_system.txt:considered that would require grantees to revise their forms or
technical/government/About_LSC/reporting_system.txt:grantees will be asked to report the number of newspaper articles
technical/government/About_LSC/reporting_system.txt:provided to grantees on quantifying the numbers of brochures and
technical/government/About_LSC/reporting_system.txt:matters data for 2002 and 2003. Some of the figures which grantees
technical/government/About_LSC/reporting_system.txt:provide to the communities served by LSC grantees.
technical/government/About_LSC/reporting_system.txt:! Informing grantees about the range of methods being used by
technical/government/About_LSC/reporting_system.txt:"story" of what LSC grantees are contributing to their communities
technical/government/About_LSC/State_Planning_Report.txt:grantees to begin to examine, on a statewide level, how all
technical/government/About_LSC/State_Planning_Report.txt:grantees in a particular state would serve in the present, and plan
technical/government/About_LSC/State_Planning_Report.txt:focused on how grantees would work together to address funding
technical/government/About_LSC/State_Planning_Report.txt:planning initiative, asking grantees to determine how they could
technical/government/About_LSC/State_Planning_Report.txt:In essence, these two Program Letters asked grantees to expand
technical/government/About_LSC/State_Planning_Report.txt:barriers and operates efficiently and effectively. LSC's grantees
technical/government/About_LSC/State_Planning_Report.txt:Letter 2000-7 renewed LSC's challenge to its grantees to actively
technical/government/About_LSC/State_Planning_Report.txt:available to grantees.
technical/government/About_LSC/State_Planning_Report.txt:for the fourteen LSC-funded grantees in the state comes from three
technical/government/About_LSC/State_Planning_Report.txt:New Jersey grantees' annual budgets comes from LSC.
technical/government/About_LSC/State_Planning_Report.txt:grantees are fully utilizing available technology to expand and
technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt:lobbying activities of LSC grantees were not "part of any special
technical/government/About_LSC/ODonnell_et_al_v_LSCdecision.txt:affect grantees. See Tex. Rural Legal Aid, Inc. v. Legal Servs.
technical/government/About_LSC/State_Planning_Special_Report.txt:partnerships with our grantees and the broader civil equal justice
technical/government/About_LSC/State_Planning_Special_Report.txt:requires its grantees in each state to work with each other and
technical/government/About_LSC/State_Planning_Special_Report.txt:therefore, feature multiple LSC-funded grantees. Others, like
technical/government/About_LSC/State_Planning_Special_Report.txt:1996 reform replacing presumptive refunding of grantees with
technical/government/About_LSC/State_Planning_Special_Report.txt:will work with the DSPB, grantees, and other stakeholders to foster
technical/government/About_LSC/State_Planning_Special_Report.txt:with its grantees and stakeholders, allowing LSC to serve as an
technical/government/About_LSC/State_Planning_Special_Report.txt:grantees and other stakeholders may have a better perspective on
technical/government/Gen_Account_Office/d0269g.txt:dollars, it is accountable for how its agencies and grantees spend
technical/government/Gen_Account_Office/d01591sp.txt:grantees sponsoring IDA programs. For fiscal year 2001, $25 million
technical/government/Media/agency_expands.txt:number of grantees in the Los Angeles area from five to three,
technical/government/Media/Annual_Fee.txt:action raising the fee "is lifesaving for our grantees," Schmitt
technical/government/Media/Barr_sharpening_ax.txt:restrictions placed on grantees are strictly observed," Erlenborn
technical/government/Media/NJ_Legal_Services.txt:requirements that apply to all LSC grantees in the country.
```
See in this example, I searched for the string "grantees". In the previous command line options, grep would have returned nothing since it wasn't going into the directories within /government. Recursively searching ensures to get every file.

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -r "Superman" technical   
adarshpatel@Adarshs-MacBook-Air docsearch % 
```
Just to make sure, we searched for "Superman" again and it doesn't seem to be in any of the files given. But as you can see, there is no output if nothing is found.

Its important to note that some of these are long and you can put commands together. With the 3 examples, lets say we want to recursively search for ONLY the word "adult" and only return the file name. We just have to put the command line options together.

```
adarshpatel@Adarshs-MacBook-Air docsearch % grep -r -w -l "adult" technical
technical/government/About_LSC/Special_report_to_congress.txt
technical/government/Env_Prot_Agen/ctf1-6.txt
technical/government/Env_Prot_Agen/ctm4-10.txt
technical/government/Env_Prot_Agen/atx1-6.txt
technical/government/Env_Prot_Agen/tech_adden.txt
technical/government/Alcohol_Problems/Session3-PDF.txt
technical/plos/pmed.0020071.txt
technical/plos/pmed.0020067.txt
technical/plos/journal.pbio.0030024.txt
technical/plos/pmed.0020103.txt
technical/plos/journal.pbio.0020232.txt
technical/plos/pmed.0020061.txt
technical/plos/journal.pbio.0030131.txt
technical/plos/journal.pbio.0020043.txt
technical/plos/pmed.0020039.txt
technical/plos/journal.pbio.0020046.txt
technical/plos/pmed.0020161.txt
technical/plos/pmed.0020015.txt
technical/plos/pmed.0020162.txt
technical/plos/pmed.0020016.txt
technical/plos/journal.pbio.0020276.txt
technical/plos/journal.pbio.0020116.txt
technical/plos/pmed.0010051.txt
technical/plos/pmed.0020009.txt
technical/plos/pmed.0020182.txt
technical/plos/journal.pbio.0020310.txt
technical/plos/pmed.0020140.txt
technical/plos/pmed.0020235.txt
technical/plos/journal.pbio.0020267.txt
technical/plos/journal.pbio.0020215.txt
technical/plos/journal.pbio.0020404.txt
technical/plos/pmed.0010026.txt
technical/plos/pmed.0020123.txt
technical/plos/pmed.0020257.txt
technical/plos/pmed.0020068.txt
technical/plos/journal.pbio.0020012.txt
technical/plos/pmed.0020242.txt
technical/biomed/1471-2350-4-3.txt
technical/biomed/1471-2156-2-3.txt
technical/biomed/1471-2156-3-11.txt
technical/biomed/1471-2466-1-1.txt
technical/biomed/1471-2202-2-9.txt
technical/biomed/gb-2003-4-4-r24.txt
technical/biomed/1471-213X-2-1.txt
technical/biomed/1471-2431-2-1.txt
technical/biomed/gb-2001-2-4-research0011.txt
technical/biomed/bcr635.txt
technical/biomed/1477-7525-1-9.txt
technical/biomed/1471-2407-3-18.txt
technical/biomed/1471-2415-3-5.txt
technical/biomed/ar130.txt
technical/biomed/gb-2002-3-7-research0032.txt
technical/biomed/1471-2202-4-10.txt
technical/biomed/gb-2003-4-4-r26.txt
technical/biomed/1472-6882-3-1.txt
technical/biomed/1471-2202-4-11.txt
technical/biomed/1471-2253-2-4.txt
technical/biomed/1471-2415-3-4.txt
technical/biomed/gb-2001-2-3-research0008.txt
technical/biomed/1471-2466-3-1.txt
technical/biomed/1472-6785-1-3.txt
technical/biomed/bcr583.txt
technical/biomed/gb-2003-4-7-r42.txt
technical/biomed/rr74.txt
technical/biomed/1471-213X-2-7.txt
technical/biomed/1476-4598-2-25.txt
technical/biomed/gb-2002-3-7-research0036.txt
technical/biomed/1471-2415-3-1.txt
technical/biomed/1471-2474-2-1.txt
technical/biomed/1471-2350-4-6.txt
technical/biomed/1471-2474-2-3.txt
technical/biomed/gb-2002-3-9-research0045.txt
technical/biomed/1471-2180-2-26.txt
technical/biomed/gb-2001-2-4-research0014.txt
technical/biomed/1471-2202-4-17.txt
technical/biomed/1472-6904-2-5.txt
technical/biomed/bcr284.txt
technical/biomed/cc2190.txt
technical/biomed/ar409.txt
technical/biomed/1471-230X-1-5.txt
technical/biomed/1471-2172-3-12.txt
technical/biomed/1471-244X-2-9.txt
technical/biomed/1471-213X-1-1.txt
technical/biomed/1471-2202-2-10.txt
technical/biomed/1471-2431-3-3.txt
technical/biomed/1471-2377-1-2.txt
technical/biomed/bcr285.txt
technical/biomed/gb-2002-3-6-software0001.txt
technical/biomed/1472-6890-1-4.txt
technical/biomed/1471-2202-2-12.txt
technical/biomed/1471-213X-1-3.txt
technical/biomed/cc1538.txt
technical/biomed/ar387.txt
technical/biomed/1471-2156-2-18.txt
technical/biomed/gb-2002-3-12-research0086.txt
technical/biomed/1471-2164-4-22.txt
technical/biomed/1471-2458-2-6.txt
technical/biomed/1477-7827-1-48.txt
technical/biomed/1471-213X-1-6.txt
technical/biomed/1472-6785-2-6.txt
technical/biomed/1477-7827-1-9.txt
technical/biomed/1471-2202-2-16.txt
technical/biomed/1472-6793-1-8.txt
technical/biomed/1472-6882-2-10.txt
technical/biomed/1471-2350-3-1.txt
technical/biomed/1471-213X-3-7.txt
technical/biomed/1471-2377-3-4.txt
technical/biomed/1471-2202-2-14.txt
technical/biomed/1471-2334-2-29.txt
technical/biomed/1471-230X-3-3.txt
technical/biomed/1471-2466-2-4.txt
technical/biomed/1471-2296-3-18.txt
technical/biomed/ar140.txt
technical/biomed/gb-2003-4-3-r17.txt
technical/biomed/1472-6793-2-11.txt
technical/biomed/1471-2202-2-15.txt
technical/biomed/gb-2002-3-12-research0080.txt
technical/biomed/cc1476.txt
technical/biomed/1471-2431-3-6.txt
technical/biomed/1477-7827-1-43.txt
technical/biomed/1472-6793-1-6.txt
technical/biomed/1471-213X-1-9.txt
technical/biomed/1471-2164-4-15.txt
technical/biomed/1471-2202-3-3.txt
technical/biomed/cc2358.txt
technical/biomed/1472-6963-3-6.txt
technical/biomed/1475-4924-1-10.txt
technical/biomed/ar429.txt
technical/biomed/1471-2334-2-24.txt
technical/biomed/1471-2156-2-12.txt
technical/biomed/1475-4924-1-5.txt
technical/biomed/cc2167.txt
technical/biomed/1477-7827-1-54.txt
technical/biomed/bcr45.txt
technical/biomed/gb-2003-4-1-r7.txt
technical/biomed/1471-2407-2-33.txt
technical/biomed/1471-2261-3-4.txt
technical/biomed/gb-2003-4-3-r18.txt
technical/biomed/1472-6793-3-6.txt
technical/biomed/1471-2202-3-1.txt
technical/biomed/1471-2350-3-9.txt
technical/biomed/1471-2164-3-26.txt
technical/biomed/gb-2002-3-5-research0021.txt
technical/biomed/1475-2867-3-3.txt
technical/biomed/1471-2121-2-15.txt
technical/biomed/rr37.txt
technical/biomed/cc1497.txt
technical/biomed/1471-2334-2-5.txt
technical/biomed/1471-2350-2-11.txt
technical/biomed/1475-2875-1-14.txt
technical/biomed/1471-2164-3-6.txt
technical/biomed/1471-2156-2-17.txt
technical/biomed/ar149.txt
technical/biomed/1471-2202-2-20.txt
technical/biomed/1472-6882-1-10.txt
technical/biomed/1471-2210-1-7.txt
technical/biomed/1471-2164-2-1.txt
technical/biomed/1477-7827-1-21.txt
technical/biomed/cvm-2-6-278.txt
technical/biomed/bcr602.txt
technical/biomed/1476-511X-2-3.txt
technical/biomed/gb-2002-3-4-research0018.txt
technical/biomed/1471-2202-2-2.txt
technical/biomed/gb-2003-4-2-r8.txt
technical/biomed/1471-2229-2-11.txt
technical/biomed/1471-2156-2-8.txt
technical/biomed/rr196.txt
technical/biomed/1472-6955-2-1.txt
technical/biomed/1471-2407-3-14.txt
technical/biomed/1471-2202-2-6.txt
technical/biomed/1471-2164-2-6.txt
technical/biomed/1471-2202-3-14.txt
technical/biomed/gb-2002-3-8-research0038.txt
technical/biomed/1471-244X-3-5.txt
technical/biomed/1471-213X-1-12.txt
technical/biomed/1471-2458-3-11.txt
technical/biomed/1468-6708-3-1.txt
technical/biomed/1472-6947-1-5.txt
technical/biomed/1471-2458-1-9.txt
technical/biomed/1471-2202-3-16.txt
technical/biomed/1471-2156-4-9.txt
technical/biomed/ar328.txt
technical/biomed/bcr605.txt
technical/biomed/1471-2210-1-3.txt
technical/biomed/1471-2334-1-13.txt
technical/biomed/1471-2202-4-2.txt
technical/biomed/bcr567.txt
technical/biomed/1471-213X-1-11.txt
technical/911report/chapter-5.txt
technical/911report/chapter-12.txt
```
We get this output. We can narrow our search results more putting the commands together.
