---
layout: page
title: Schedule & Material
---

## Lecture schedule

The course plan is subject to change.
The slides of future classes are linked
to the slides from the [last year's course](http://www.sfs.uni-tuebingen.de/~ddekok/dsa3/).
<em>However, slides with a (*) have been updated.</em>
'A' below indicates the noon session starting at 12:15,
and 'B' indicates the evening sessions starting at 18:00.

<table rules="groups" style="width:100%;border-collapse: collapse;">
  <thead style="border-bottom: 1px solid #000;">
    <tr>
      <th style="text-align:left;" width="10%">Week</th>
      <th style="text-align:left;" width="30%">Monday (lectures)</th>
      <th style="text-align:left;" width="30%">Wednesday (lab)</th>
    </tr>
  </thead>
  <tbody style="border-bottom: 1px solid #000;">
{% for week in site.data.schedule %}
    <tr style="border-bottom: 1px solid #000;">
    <td style="text-align:left;"> {{ week.week }} </td>
    {% for date in week.dates %}
            <td valign="top"> {{ date[0] }} <br/>
                {% if date[1].topics %}
                    {% for topic in date[1].topics %}
                        {{ topic[0] }}: <em> {{ topic[1] }}</em>{% unless forloop.last %}<br/> {% endunless %}
                    {% endfor %}
                {% else %}
                    <em style="color: red">No class</em>
                {% endif %}
                {% if date[1].links %}
                    <br/>
                    [{% for link in date[1].links %}<a href="{{ link[1] }}">{{ link[0] }}</a>{% unless forloop.last %}, {% endunless %}{% endfor %}]
                {% endif %}
                {% if date[1].reading %}
                    <br/>
                    Reading: {{ date[1].reading }}
                {% endif %}
            </td>
    {% endfor %}
    </tr>
{% endfor %}
  </tbody>
</table>


## Extra Reading and Lecture Material

<ul>
<li><a href="material/CavnarTrenkle.pdf">Language Guessing (Cavnar and Trenkle, 1994)</a> </li>
<li><a href="slides/21DemoSelectionSort.pdf">Animation for Selection Sort</a> </li>
<li><a href="slides/21DemoInsertionSort.pdf">Animation for Insertion Sort</a> </li>
<li><a href="slides/21DemoShellSort.pdf">Animation for Shell Sort</a> </li>
<li><a href="slides/21DemoKnuthShuffle.pdf">Animation for Knuth Shuffle</a> </li>
<li><a href="slides/23DemoPartitioning.pdf">Animation of Quicksort partitionings</a> </li>
<li><a href="slides/24DemoBinaryHeap.pdf">Animation for Binary Heap</a> </li>
<li><a href="slides/24DemoHeapsort.pdf">Animation for Heapsort</a> </li>
<li><a href="slides/41DemoDepthFirstSearch.pdf">Animation for DFS in graphs</a></li>
<li><a href="slides/41DemoBreadthFirstSearch.pdf">Animation for BFS in graphs</a></li>
<li><a href="slides/41DemoConnectedComponents.pdf">Animation for graph connectedness</a></li>

<li><a href="slides/42DemoDepthFirstSearch.pdf">Animation for DFS in directed graphs</a></li>
<li><a href="slides/42DemoBreadthFirstSearch.pdf">Animation for BFS in directed graphs</a></li>
<li><a href="slides/42DemoKosarajuSharir.pdf">Animation for Kosaraju-Sharir algorithm</a></li>
<li><a href="slides/42DemoTopologicalSort.pdf">Animation for Topological sort algorithm</a></li>

<li><a href="slides/43DemoGreedy.pdf">Animation for Greedy Algorithm</a></li>
<li><a href="slides/43DemoKruskal.pdf">Animation for Kruskal's Algorithm</a></li>
<li><a href="slides/43DemoPrim.pdf">Animation for Prim's Algorithm</a></li>

<li><a href="slides/44DemoDijkstra.pdf">Animation for Dijkstra's Algorithm</a></li>
<li><a href="slides/44DemoAcyclicSP.pdf">Animation for Acyclic Shortest Paths</a></li>
<li><a href="slides/44DemoBellmanFord.pdf">Animation for 44 Bellman-Ford Algorithm</a></li>
</ul>

