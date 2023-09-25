Code Chunk: Knitr & Kable Extra Tables for Research Purposes
================

## Why this table?

Welcome to my Knitr Table page! Hopefully this code chunk will make
your life easier when making a complex table.

The knitrtable code chunk in the example below can be a
helpful resource for creating organized and beautiful looking tables.

The following example and data comes from a similar dataset to a study
on freshwater availability in Sub-Saharan Africa [^1]. This table was an
attempt to recreate the table used in the Pickering and Davis study.

## Set Up!

Creating these easy tables will include the following setup. As usual,
please make sure to set your working directory and then install the
following packages:

To try the example yourself, you can find the dataset above labeled
`ssa_water.Rdata`

## Try an Example

Don’t take it from me, try the following table for yourself!

``` r
df3 %>%
  kable(.,align = "c", 
        caption = "Table 1. Household Survey Observations (n = 199 067) from 28 Countries in Sub-Saharan Africa$^a$", 
        caption_position = "top_left") %>%
  add_header_above(c(" " = 3, 
                     "walk time (min)" = 3, 
                     " " = 1), 
                   line = 2, 
                   bold = TRUE, 
                   escape = FALSE, 
                   background = "#d3d3d3") %>%
  kable_classic(full_width = F) %>%
  row_spec(0, background = "#d3d3d3") %>%
  footnote(alphabet = c(
    "Number of observations are shown from each country, as well as year(s) of survey, mean one-way walk time to water source in minutes (min), standard deviation of mean walk time (SD), median walk time (med), and percent of households with water source located on the premises (% on plot)." 
    )) 
```

<table class=" lightable-classic" style="font-family: &quot;Arial Narrow&quot;, &quot;Source Sans Pro&quot;, sans-serif; width: auto !important; margin-left: auto; margin-right: auto;border-bottom: 0;">
<caption>
Table 1. Household Survey Observations (n = 199 067) from 28 Countries
in Sub-Saharan Africa$^a$
</caption>
<thead>
<tr>
<th style="empty-cells: hide;border-bottom:hidden;" colspan="3">
</th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-weight: bold; padding-right: 4px; padding-left: 4px; background-color: #d3d3d3 !important;" colspan="3">

<div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">

walk time (min)

</div>

</th>
<th style="empty-cells: hide;border-bottom:hidden;" colspan="1">
</th>
</tr>
<tr>
<th style="text-align:center;background-color: #d3d3d3 !important;">
country
</th>
<th style="text-align:center;background-color: #d3d3d3 !important;">
N
</th>
<th style="text-align:center;background-color: #d3d3d3 !important;">
year
</th>
<th style="text-align:center;background-color: #d3d3d3 !important;">
mean
</th>
<th style="text-align:center;background-color: #d3d3d3 !important;">
SD
</th>
<th style="text-align:center;background-color: #d3d3d3 !important;">
med
</th>
<th style="text-align:center;background-color: #d3d3d3 !important;">
% on plot
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center;">
BF6
</td>
<td style="text-align:center;">
28849
</td>
<td style="text-align:center;">
2010-2010
</td>
<td style="text-align:center;">
20.30765
</td>
<td style="text-align:center;">
18.96601
</td>
<td style="text-align:center;">
15
</td>
<td style="text-align:center;">
9
</td>
</tr>
<tr>
<td style="text-align:center;">
BJ6
</td>
<td style="text-align:center;">
32486
</td>
<td style="text-align:center;">
2011-2012
</td>
<td style="text-align:center;">
14.31397
</td>
<td style="text-align:center;">
30.77288
</td>
<td style="text-align:center;">
5
</td>
<td style="text-align:center;">
34
</td>
</tr>
<tr>
<td style="text-align:center;">
CD6
</td>
<td style="text-align:center;">
33656
</td>
<td style="text-align:center;">
2013-2014
</td>
<td style="text-align:center;">
33.29898
</td>
<td style="text-align:center;">
30.86483
</td>
<td style="text-align:center;">
30
</td>
<td style="text-align:center;">
6
</td>
</tr>
<tr>
<td style="text-align:center;">
CI6
</td>
<td style="text-align:center;">
16298
</td>
<td style="text-align:center;">
2011-2012
</td>
<td style="text-align:center;">
14.91906
</td>
<td style="text-align:center;">
29.28821
</td>
<td style="text-align:center;">
5
</td>
<td style="text-align:center;">
43
</td>
</tr>
<tr>
<td style="text-align:center;">
CM6
</td>
<td style="text-align:center;">
24163
</td>
<td style="text-align:center;">
2011-2011
</td>
<td style="text-align:center;">
20.30567
</td>
<td style="text-align:center;">
27.45360
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
17
</td>
</tr>
<tr>
<td style="text-align:center;">
ET6
</td>
<td style="text-align:center;">
27715
</td>
<td style="text-align:center;">
2003-2003
</td>
<td style="text-align:center;">
52.50238
</td>
<td style="text-align:center;">
71.83227
</td>
<td style="text-align:center;">
30
</td>
<td style="text-align:center;">
13
</td>
</tr>
<tr>
<td style="text-align:center;">
GA6
</td>
<td style="text-align:center;">
12854
</td>
<td style="text-align:center;">
2012-2012
</td>
<td style="text-align:center;">
21.40812
</td>
<td style="text-align:center;">
36.04820
</td>
<td style="text-align:center;">
5
</td>
<td style="text-align:center;">
45
</td>
</tr>
<tr>
<td style="text-align:center;">
GH5
</td>
<td style="text-align:center;">
15697
</td>
<td style="text-align:center;">
2008-2008
</td>
<td style="text-align:center;">
18.22342
</td>
<td style="text-align:center;">
26.30430
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
16
</td>
</tr>
<tr>
<td style="text-align:center;">
GN6
</td>
<td style="text-align:center;">
16380
</td>
<td style="text-align:center;">
2012-2012
</td>
<td style="text-align:center;">
23.26777
</td>
<td style="text-align:center;">
24.87105
</td>
<td style="text-align:center;">
20
</td>
<td style="text-align:center;">
23
</td>
</tr>
<tr>
<td style="text-align:center;">
KE5
</td>
<td style="text-align:center;">
13105
</td>
<td style="text-align:center;">
2008-2009
</td>
<td style="text-align:center;">
27.99992
</td>
<td style="text-align:center;">
40.75140
</td>
<td style="text-align:center;">
15
</td>
<td style="text-align:center;">
28
</td>
</tr>
<tr>
<td style="text-align:center;">
KM6
</td>
<td style="text-align:center;">
8141
</td>
<td style="text-align:center;">
2012-2012
</td>
<td style="text-align:center;">
10.33154
</td>
<td style="text-align:center;">
24.79671
</td>
<td style="text-align:center;">
0
</td>
<td style="text-align:center;">
69
</td>
</tr>
<tr>
<td style="text-align:center;">
LB6
</td>
<td style="text-align:center;">
16229
</td>
<td style="text-align:center;">
2013-2013
</td>
<td style="text-align:center;">
17.05797
</td>
<td style="text-align:center;">
19.16343
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
8
</td>
</tr>
<tr>
<td style="text-align:center;">
LS5
</td>
<td style="text-align:center;">
14300
</td>
<td style="text-align:center;">
2009-2010
</td>
<td style="text-align:center;">
20.14084
</td>
<td style="text-align:center;">
24.04501
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
13
</td>
</tr>
<tr>
<td style="text-align:center;">
MD5
</td>
<td style="text-align:center;">
31744
</td>
<td style="text-align:center;">
2008-2009
</td>
<td style="text-align:center;">
16.69193
</td>
<td style="text-align:center;">
41.38327
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
15
</td>
</tr>
<tr>
<td style="text-align:center;">
ML6
</td>
<td style="text-align:center;">
20598
</td>
<td style="text-align:center;">
2012-2013
</td>
<td style="text-align:center;">
10.17318
</td>
<td style="text-align:center;">
27.79201
</td>
<td style="text-align:center;">
3
</td>
<td style="text-align:center;">
37
</td>
</tr>
<tr>
<td style="text-align:center;">
MW5
</td>
<td style="text-align:center;">
43732
</td>
<td style="text-align:center;">
2010-2010
</td>
<td style="text-align:center;">
29.90817
</td>
<td style="text-align:center;">
31.87291
</td>
<td style="text-align:center;">
20
</td>
<td style="text-align:center;">
9
</td>
</tr>
<tr>
<td style="text-align:center;">
MZ6
</td>
<td style="text-align:center;">
22075
</td>
<td style="text-align:center;">
2011-2011
</td>
<td style="text-align:center;">
29.18957
</td>
<td style="text-align:center;">
49.97817
</td>
<td style="text-align:center;">
15
</td>
<td style="text-align:center;">
24
</td>
</tr>
<tr>
<td style="text-align:center;">
NG6
</td>
<td style="text-align:center;">
58812
</td>
<td style="text-align:center;">
2013-2013
</td>
<td style="text-align:center;">
20.33144
</td>
<td style="text-align:center;">
29.20488
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
21
</td>
</tr>
<tr>
<td style="text-align:center;">
NM6
</td>
<td style="text-align:center;">
12171
</td>
<td style="text-align:center;">
2013-2013
</td>
<td style="text-align:center;">
13.99334
</td>
<td style="text-align:center;">
26.47023
</td>
<td style="text-align:center;">
0
</td>
<td style="text-align:center;">
50
</td>
</tr>
<tr>
<td style="text-align:center;">
RW6
</td>
<td style="text-align:center;">
19246
</td>
<td style="text-align:center;">
2010-2011
</td>
<td style="text-align:center;">
36.39345
</td>
<td style="text-align:center;">
33.44114
</td>
<td style="text-align:center;">
30
</td>
<td style="text-align:center;">
6
</td>
</tr>
<tr>
<td style="text-align:center;">
SL6
</td>
<td style="text-align:center;">
25749
</td>
<td style="text-align:center;">
2013-2013
</td>
<td style="text-align:center;">
21.04759
</td>
<td style="text-align:center;">
22.97983
</td>
<td style="text-align:center;">
15
</td>
<td style="text-align:center;">
10
</td>
</tr>
<tr>
<td style="text-align:center;">
SN6
</td>
<td style="text-align:center;">
26564
</td>
<td style="text-align:center;">
2010-2011
</td>
<td style="text-align:center;">
12.25503
</td>
<td style="text-align:center;">
31.27550
</td>
<td style="text-align:center;">
0
</td>
<td style="text-align:center;">
54
</td>
</tr>
<tr>
<td style="text-align:center;">
SZ5
</td>
<td style="text-align:center;">
8025
</td>
<td style="text-align:center;">
2006-2007
</td>
<td style="text-align:center;">
21.12428
</td>
<td style="text-align:center;">
30.88023
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
32
</td>
</tr>
<tr>
<td style="text-align:center;">
TG6
</td>
<td style="text-align:center;">
16280
</td>
<td style="text-align:center;">
2013-2014
</td>
<td style="text-align:center;">
23.70795
</td>
<td style="text-align:center;">
29.45507
</td>
<td style="text-align:center;">
15
</td>
<td style="text-align:center;">
13
</td>
</tr>
<tr>
<td style="text-align:center;">
TZ5
</td>
<td style="text-align:center;">
17251
</td>
<td style="text-align:center;">
2009-2010
</td>
<td style="text-align:center;">
29.99512
</td>
<td style="text-align:center;">
39.11909
</td>
<td style="text-align:center;">
16
</td>
<td style="text-align:center;">
13
</td>
</tr>
<tr>
<td style="text-align:center;">
UG6
</td>
<td style="text-align:center;">
16740
</td>
<td style="text-align:center;">
2011-2011
</td>
<td style="text-align:center;">
45.74853
</td>
<td style="text-align:center;">
49.90601
</td>
<td style="text-align:center;">
30
</td>
<td style="text-align:center;">
10
</td>
</tr>
<tr>
<td style="text-align:center;">
ZM6
</td>
<td style="text-align:center;">
30871
</td>
<td style="text-align:center;">
2013-2014
</td>
<td style="text-align:center;">
17.68385
</td>
<td style="text-align:center;">
23.84441
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
24
</td>
</tr>
<tr>
<td style="text-align:center;">
ZW6
</td>
<td style="text-align:center;">
14195
</td>
<td style="text-align:center;">
2010-2011
</td>
<td style="text-align:center;">
19.45173
</td>
<td style="text-align:center;">
30.33077
</td>
<td style="text-align:center;">
10
</td>
<td style="text-align:center;">
35
</td>
</tr>
</tbody>
<tfoot>
<tr>
<td style="padding: 0; " colspan="100%">
<sup>a</sup> Number of observations are shown from each country, as well
as year(s) of survey, mean one-way walk time to water source in minutes
(min), standard deviation of mean walk time (SD), median walk time
(med), and percent of households with water source located on the
premises (% on plot).
</td>
</tr>
</tfoot>
</table>

You can see from the code and output what this code is capable of. You
easily have full control over the caption, header, background, table
style (as seen with the `kable_classic` code), and footnote.

## In Conclusion

As a student that is looking to go on to get a PhD, this code chunk is a
good example that I can take and use for other projects. Since it has a
clear style with the `kable_classic` line of code, it can easily be used
for research papers.

[^1]: Pickering, A. J., & Davis, J. (2012). Freshwater availability and
    water fetching distance affect child health in Sub-Saharan africa.
    Environmental Science &amp; Technology, 46(4), 2391–2397.
    <https://doi.org/10.1021/es203177v>
