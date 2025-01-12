
<!DOCTYPE html
  PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html><head>
      <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
   <!--
This HTML was auto-generated from MATLAB code.
To make changes, update the MATLAB code and republish this document.
      --><title>Readme_showM</title><meta name="generator" content="MATLAB 9.6"><link rel="schema.DC" href="http://purl.org/dc/elements/1.1/"><meta name="DC.date" content="2019-10-04"><meta name="DC.source" content="Readme_showM.m"><style type="text/css">
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,font,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td{margin:0;padding:0;border:0;outline:0;font-size:100%;vertical-align:baseline;background:transparent}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:'';content:none}:focus{outine:0}ins{text-decoration:none}del{text-decoration:line-through}table{border-collapse:collapse;border-spacing:0}

html { min-height:100%; margin-bottom:1px; }
html body { height:100%; margin:0px; font-family:Arial, Helvetica, sans-serif; font-size:10px; color:#000; line-height:140%; background:#fff none; overflow-y:scroll; }
html body td { vertical-align:top; text-align:left; }

h1 { padding:0px; margin:0px 0px 25px; font-family:Arial, Helvetica, sans-serif; font-size:1.5em; color:#d55000; line-height:100%; font-weight:normal; }
h2 { padding:0px; margin:0px 0px 8px; font-family:Arial, Helvetica, sans-serif; font-size:1.2em; color:#000; font-weight:bold; line-height:140%; border-bottom:1px solid #d6d4d4; display:block; }
h3 { padding:0px; margin:0px 0px 5px; font-family:Arial, Helvetica, sans-serif; font-size:1.1em; color:#000; font-weight:bold; line-height:140%; }

a { color:#005fce; text-decoration:none; }
a:hover { color:#005fce; text-decoration:underline; }
a:visited { color:#004aa0; text-decoration:none; }

p { padding:0px; margin:0px 0px 20px; }
img { padding:0px; margin:0px 0px 20px; border:none; }
p img, pre img, tt img, li img, h1 img, h2 img { margin-bottom:0px; } 

ul { padding:0px; margin:0px 0px 20px 23px; list-style:square; }
ul li { padding:0px; margin:0px 0px 7px 0px; }
ul li ul { padding:5px 0px 0px; margin:0px 0px 7px 23px; }
ul li ol li { list-style:decimal; }
ol { padding:0px; margin:0px 0px 20px 0px; list-style:decimal; }
ol li { padding:0px; margin:0px 0px 7px 23px; list-style-type:decimal; }
ol li ol { padding:5px 0px 0px; margin:0px 0px 7px 0px; }
ol li ol li { list-style-type:lower-alpha; }
ol li ul { padding-top:7px; }
ol li ul li { list-style:square; }

.content { font-size:1.2em; line-height:140%; padding: 20px; }

pre, code { font-size:12px; }
tt { font-size: 1.2em; }
pre { margin:0px 0px 20px; }
pre.codeinput { padding:10px; border:1px solid #d3d3d3; background:#f7f7f7; }
pre.codeoutput { padding:10px 11px; margin:0px 0px 20px; color:#4c4c4c; }
pre.error { color:red; }

@media print { pre.codeinput, pre.codeoutput { word-wrap:break-word; width:100%; } }

span.keyword { color:#0000FF }
span.comment { color:#228B22 }
span.string { color:#A020F0 }
span.untermstring { color:#B20000 }
span.syscmd { color:#B28C00 }

.footer { width:auto; padding:10px 0px; margin:25px 0px 0px; border-top:1px dotted #878787; font-size:0.8em; line-height:140%; font-style:italic; color:#878787; text-align:left; float:none; }
.footer p { margin:0px; }
.footer a { color:#878787; }
.footer a:hover { color:#878787; text-decoration:underline; }
.footer a:visited { color:#878787; }

table th { padding:7px 5px; text-align:left; vertical-align:middle; border: 1px solid #d6d4d4; font-weight:bold; }
table td { padding:7px 5px; text-align:left; vertical-align:top; border:1px solid #d6d4d4; }





  </style></head><body><div class="content"><h1></h1><!--introduction--><!--/introduction--><h2>Contents</h2><div><ul><li><a href="#1">Using showM</a></li><li><a href="#2">Repo location</a></li><li><a href="#3">Intro</a></li><li><a href="#4">For the expert/impatient</a></li><li><a href="#10">Inputs and examples</a></li><li><a href="#18">Showing data from only a few networks</a></li><li><a href="#19">Showing data from only specific systems</a></li><li><a href="#20">Get color limits based on the systems you care</a></li><li><a href="#21">Credits and date</a></li></ul></div><h2 id="1">Using showM</h2><h2 id="2">Repo location</h2><p>This function belongs to the package "plotting tools".</p><p>https://gitlab.com/ascario/plotting-tools</p><h2 id="3">Intro</h2><p>This code visualize connectivioty matrices. The most basic functionality is to only display a 2d matrices. If you provide extra (optional) arguments, you can group connectivity values per functional system and mess with coloring schema and visualization ranges.</p><h2 id="4">For the expert/impatient</h2><p>Example 1</p><p>Using the most basic functionality</p><pre class="codeinput">showM(M);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_01.png" alt=""> <p>Example 2</p><p>Using a lot of options</p><pre class="codeinput"> showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5,<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.3 .39],<span class="keyword">...</span>
    <span class="string">'fs_axis'</span>,10,<span class="keyword">...</span>
    <span class="string">'fig_wide'</span>,7,<span class="keyword">...</span>
    <span class="string">'one_side_labels'</span>,1,<span class="keyword">...</span>
    <span class="string">'fig_tall'</span>,8);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_02.png" alt=""> <pre class="codeinput"> showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,<span class="string">'RG'</span>,<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.3 .39],<span class="keyword">...</span>
    <span class="string">'half'</span>,<span class="string">'both'</span>);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_03.png" alt=""> <pre class="codeinput"> showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,<span class="string">'RG'</span>,<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.3 .39],<span class="keyword">...</span>
    <span class="string">'half'</span>,<span class="string">'up'</span>);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_04.png" alt=""> <pre class="codeinput"> showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,<span class="string">'RG'</span>,<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.3 .39],<span class="keyword">...</span>
    <span class="string">'one_side_labels'</span>,1,<span class="keyword">...</span>
    <span class="string">'half'</span>,<span class="string">'low'</span>);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_05.png" alt=""> <h2 id="10">Inputs and examples</h2><p><b>MANDATORY</b></p><p><b>M</b>: A connectivity matrix size ROIxROI.</p><pre class="codeinput">showM(M);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_06.png" alt=""> <p><b>OPTIONAL (provided as paired arguments 'Name,Value')</b></p><div><ul><li><b>'clims',Value</b>, clims define the limots to be used vor visualization. 'Value' is a vector with the minimum and maximum value to be used for visualization. If not provided, the code will use as limits the minimun and maximum of M.</li></ul></div><p>Example 1</p><p>Lets use [-.5 .5] as limits of visualization</p><pre class="codeinput">minmax=[-.5 .5];
showM(M,<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.5 .5]);
title([<span class="string">'Using ['</span>, num2str(minmax(1) ), <span class="string">' '</span> num2str(minmax(2)), <span class="string">'] as limits'</span>])
<span class="comment">%</span>
<span class="comment">% Example 2</span>
<span class="comment">%</span>
<span class="comment">% Let's remove extreme values from the connectivity matrices</span>
delta=.1;<span class="comment">% how much (percentile) of the data to exclude</span>
values=M(tril(M)==0); <span class="comment">%excluding values of the diagonal</span>
ptiles=[delta 100-delta]; <span class="comment">%percentiles to incluide</span>
minmax=prctile(values,ptiles);
showM(M,<span class="keyword">...</span>
    <span class="string">'clims'</span>,minmax);
title([<span class="string">'Using ['</span>, num2str(minmax(1) ), <span class="string">' '</span> num2str(minmax(2)), <span class="string">'] as limits'</span>])
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_07.png" alt=""> <img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_08.png" alt=""> <div><ul><li><b>'parcel',Value</b>, Here you can define the assignment of each ROI to a functional system. Value must be an structure whos size equals the number of functional systems and it must contain as fields the name and indices assigned to each functional system. YOu can inspect the included structure parcel that defines the Gordon parcelation schema</li></ul></div><p>Example</p><pre class="codeinput">showM(M,<span class="string">'parcel'</span>,parcel);
<span class="comment">%</span>
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_09.png" alt=""> <div><ul><li><b>'one_side_labels',Value</b>. Value is 1 or 0 and indicates if you like the labels with the names of the functional system in one side or both sides of the matrix. Default is 0.</li></ul></div><p>Example</p><pre class="codeinput">showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'one_side_labels'</span>,1);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_10.png" alt=""> <p><b>'line_width',Value</b>. Line width for dividers. Default is 1.</p><p>Example</p><pre class="codeinput">showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_width'</span>,1.5);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_11.png" alt=""> <p>*line_color',Value'. Color to be used for the divider lines. If provided, must be a 3 elements vector with the RGB values of the color to be used. Default is white ([1 1 1])</p><p>Example</p><pre class="codeinput">showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_12.png" alt=""> <div><ul><li>*'show_dividers,Value'*Value is 1 or 0 and indicates whether you want lines to be displayed to separate functional systems. Default is 1</li></ul></div><pre class="codeinput">showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'show_dividers'</span>,0);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_13.png" alt=""> <div><ul><li><b>'my_color',Value</b>. Predefined coloring schemas. Only availabe options are red-blue (<b>RB</b>, default), red-yellow-blue ('RYB'), and red-green ('RG'). If unhappy, you can always force jet, parula or any other matlab schema</li></ul></div><p>Example</p><pre class="codeinput">my_color=cell(3,1);
my_color{1}=<span class="string">'RB'</span>;
my_color{2}=<span class="string">'RYB'</span>;
my_color{3}=<span class="string">'RG'</span>;
<span class="keyword">for</span> i=1:3
    showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,my_color{i},<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.3 .39]);
<span class="keyword">end</span>

showM(M,<span class="keyword">...</span>
    <span class="string">'parcel'</span>,parcel,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,[0 0 0],<span class="keyword">...</span>
    <span class="string">'line_width'</span>,0.5,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,my_color{i},<span class="keyword">...</span>
    <span class="string">'clims'</span>,[-.3 .39]);
colormap <span class="string">jet</span>
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_14.png" alt=""> <img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_15.png" alt=""> <img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_16.png" alt=""> <img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_17.png" alt=""> <h2 id="18">Showing data from only a few networks</h2><p>If you want to show data from only a few networks, you need to make a new parcel object that only includes the networks you care. For example, if you just care about motor, subcortical and default, those systems in the provided sturcture <b>parcel</b> has the following indices: 8, 9 13, and 4.</p><p>The companion function and the following lines of code might help to get this thing done</p><pre class="codeinput">n_systems=size(parcel,2); <span class="comment">% count the number of functional systems in the object parcel</span>
ix_networks_to_keep=[8 9 13 4];<span class="comment">% indices to keep</span>
ix_networks_to_remove=get_ix_networks_to_remove(ix_networks_to_keep,n_systems); <span class="comment">% get the indices of the systems to remove</span>

<span class="comment">% calculate the new truncated parcel abject and the corresponding truncated</span>
<span class="comment">% matrix with the indices properly sorted</span>
[newM, newParcel]=truncate_parcel_resort_matrix(M,parcel,ix_networks_to_remove);
<span class="comment">%</span>
<span class="comment">% Calculate color limits excluding a delta of one on each tale</span>
delta=1;
clims=get_ptiles_M(newM,delta);
<span class="comment">%</span>
<span class="comment">% Define options for plotting</span>
fig_wide=8;
fig_tall=9;
line_color=[1 1 1]*0;
one_side_labels=1;
half=<span class="string">'low'</span>;
line_width=.01;
my_color=<span class="string">'RB'</span>;
<span class="comment">%</span>
<span class="comment">% Display the new matrix</span>
showM(newM,<span class="string">'parcel'</span>,newParcel,<span class="keyword">...</span>
    <span class="string">'clims'</span>,clims,<span class="keyword">...</span>
    <span class="string">'fig_tall'</span>,fig_tall,<span class="keyword">...</span>
    <span class="string">'fig_wide'</span>,fig_wide,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,line_color,<span class="keyword">...</span>
    <span class="string">'one_side_labels'</span>,one_side_labels,<span class="keyword">...</span>
    <span class="string">'half'</span>,half,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,my_color,<span class="keyword">...</span>
    <span class="string">'line_width'</span>,line_width);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_18.png" alt=""> <h2 id="19">Showing data from only specific systems</h2><p>If you want to only show data from particular systems, you need to provide the list of the pairs you care. Building on the previous example, if you only like to show data from the Def-Def, Def-Sml and Sub-SMm on the truncated parcel, you need to identify the indices:</p><p>count systems in the new parcel</p><pre class="codeinput">n_systems=size(newParcel,2);
<span class="comment">%</span>
<span class="comment">% Display the indices</span>
[num2str([1:n_systems]') repmat(<span class="string">') '</span>,n_systems,1) cat(1,char(newParcel.name)) repmat(<span class="string">', n = '</span>,n_systems,1) num2str(cat(1,newParcel.n))]
<span class="comment">%</span>
<span class="comment">% Report the indices</span>
ix_parcel_pairs_on=[1 1; 2 3; 3 4];

showM(newM,<span class="string">'parcel'</span>,newParcel,<span class="keyword">...</span>
    <span class="string">'clims'</span>,clims,<span class="keyword">...</span>
    <span class="string">'fig_tall'</span>,fig_tall,<span class="keyword">...</span>
    <span class="string">'fig_wide'</span>,fig_wide,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,line_color,<span class="keyword">...</span>
    <span class="string">'one_side_labels'</span>,one_side_labels,<span class="keyword">...</span>
    <span class="string">'half'</span>,half,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,my_color,<span class="keyword">...</span>
    <span class="string">'line_width'</span>,line_width,<span class="keyword">...</span>
    <span class="string">'IX_parcel_pairs_ON'</span>,ix_parcel_pairs_on);
</pre><pre class="codeoutput">
ans =

  4&times;22 char array

    '1) Def        , n = 41'
    '2) Sml        , n = 38'
    '3) SMm        , n =  8'
    '4) Subcortical, n = 19'

</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_19.png" alt=""> <h2 id="20">Get color limits based on the systems you care</h2><p>This function calculate color limits based</p><pre class="codeinput">clims=get_ptiles_M_from_pairs(newM,delta,newParcel,ix_parcel_pairs_on);
showM(newM,<span class="string">'parcel'</span>,newParcel,<span class="keyword">...</span>
    <span class="string">'clims'</span>,clims,<span class="keyword">...</span>
    <span class="string">'fig_tall'</span>,fig_tall,<span class="keyword">...</span>
    <span class="string">'fig_wide'</span>,fig_wide,<span class="keyword">...</span>
    <span class="string">'line_color'</span>,line_color,<span class="keyword">...</span>
    <span class="string">'one_side_labels'</span>,one_side_labels,<span class="keyword">...</span>
    <span class="string">'half'</span>,half,<span class="keyword">...</span>
    <span class="string">'my_color'</span>,my_color,<span class="keyword">...</span>
    <span class="string">'line_width'</span>,line_width,<span class="keyword">...</span>
    <span class="string">'IX_parcel_pairs_ON'</span>,ix_parcel_pairs_on);
</pre><img vspace="5" hspace="5" src="https://raw.githubusercontent.com/norabyington/dcan_rtd/master/docs/visual/show/readme_showM/Readme_showM_20.png" alt=""> <h2 id="21">Credits and date</h2><p>Code developed by Oscar Miranda-Dominguez.</p><p>First line of code: July 5, 2018</p><p>Documentation started on May 24, 2019</p><p class="footer"><br><a href="https://www.mathworks.com/products/matlab/">Published with MATLAB&reg; R2019a</a><br></p></div></body></html>
