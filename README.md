TK::GraphMan - A scrolling Windows Task Manager style grid/graph chart

<h2 id="SYNOPSIS">SYNOPSIS</h2>

```perl
use strict;
use warnings;
use Tk;
use Tk::GraphMan;
my $main = new MainWindow();
my $grid1 = $main-&gt;GraphMan( -interval =&gt; 250 )-&gt;pack();
$grid1-&gt;Tk::GraphMan::start();
#do something to generate numeric data for graphing to the chart...
$grid1-&gt;Tk::GraphMan::data(100); #add an integer to the graph&#39;s timeline, in scalar context
# or ...
$grid1-&gt;Tk::GraphMan::data_array(35,36,37,38,39,40,38,36,33); #add an integer to the graph&#39;s timeline, in array context
$main-&gt;MainLoop();
```
<h2 id="REQUIRES">REQUIRES</h2>

<pre><code>  Tk</code></pre>

<h2 id="DESCRIPTION">DESCRIPTION</h2>
A scrolling Windows Task Manager style grid/graph chart. This is a Tk::Canvas widget that has the look and feel of the Windows Task Manager grid/graph chart.

<h2 id="WIDGET-SPECIFIC-OPTIONS">WIDGET-SPECIFIC OPTIONS</h2>

<pre><code>  -bgcolor
  Specify the background color of the chart.  (Default is &#39;black&#39;)

  -grid_color
  Specify the vertical and horizontal grid line colors of the chart.  (Default is &#39;#008040&#39;)

  -data_color
  Color of the data being displayed plotted on the chart.  (Default is &#39;green&#39;)

  -interval(milliseconds)
  This options determines how frequently to scroll the chart.

  -height
  Sets the height of the chart, in pixels.  (Default is 100)

  -width
  Sets the width of the chart, in pixels.  (Default is 230)

  -data_title
  Name of the data being displayed.  This is only used when the -showvalues option is set to &#39;on&#39;.  (Default is &#39;Data&#39;)

  -text_color
  Sets the text color of the -data_title option.  This is only used when the -showvalues option is set to &#39;on&#39;.  (Default is &#39;white&#39;)

  -showvalues(&#39;on&#39;|&#39;off&#39;)
  This option toggles printing of the current value (value on the far right of the chart) on and off.  (Default is &#39;off&#39;)

  -centerline(&#39;on&#39;|&#39;off&#39;)
  This option toggles a line to be drawn horizontally in the center of the graph.  (Default is &#39;off&#39;)

  -centerline_color
  Sets the color of the centerline.  This is only used when the -centerline option is set to &#39;on&#39;.  (Default is &#39;#ff0000&#39;)</code></pre>

<h2 id="METHODS">METHODS</h2>

<h4 id="start">start()</h4>

<pre><code>  Begin scrolling the chart.  The chart scrolls to the left, just like the Windows Task Manager chart.</code></pre>

<h4 id="stop">stop()</h4>

<pre><code>  Stop scrolling the chart.</code></pre>

<h4 id="data-data">data($data)</h4>

<pre><code>  Plot a number stored in $data scalar on the chart.  Value will be added to the right-side of the chart.</code></pre>

<h4 id="data_array-data">data_array(@data)</h4>

<pre><code>  Plot a list of numbers stored in @data array on the chart.  Values will be added to the right-side of the chart.</code></pre>

<h3 id="AUTHOR">AUTHOR</h3>

<p>Brett Carroll, &lt;bcarroll@cpan.org&gt;</p>
