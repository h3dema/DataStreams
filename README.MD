# Data Streams

## Surveys:
* Survey by Liberty and Nelson: http://www.cs.yale.edu/homes/el327/papers/streaming_data_mining.pdf
* Survey by Lin and Zhang: http://www.cse.unsw.edu.au/~yingz/papers/apweb_2008.pdf
Survey by G. Cormode: http://dimacs.rutgers.edu/~graham/pubs/papers/sk.pdf
Good general survey of distinct element counting up to 2008: Ahmed Metwally, Divyakant Agrawal, Amr El Abbadi: Why go logarithmic if we can go linear?: Towards effective distinct counting of search traffic. EDBT 2008: 618-629.

## Bibliography:
* A very general bibliography by K. Tufte: http://web.cecs.pdx.edu/~tufte/410-510DS/readings.htm

## Books
* Book by G. Cormode, M. Garofalakis, P. Haas, and C. Jermain:http://dimacs.rutgers.edu/~graham/pubs/html/CormodeGarofalakisHaasJermaine12.html

## Lecture Notes, and Presentations
* Lecture notes by A. Chakrabarti: http://www.cs.dartmouth.edu/~ac/Teach/CS85-Fall09/Notes/lecnotes.pdf
* Presentation including some sketches: http://www.cs.upc.edu/~conrado/research/talks/aofa2012.pdf
* MIRI Seminar on Data Streams, spring 2015 edition
  * Lecture 1: [The data stream model. Counting. Probability tools](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture1.pdf)
  * Lecture 2. [Frequency problems](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture2.pdf)
  * Lecture 3. [Sampling. Finding frequent elements. The CM-sketch](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture3.pdf)
  * Lecture 4. [Distributed sketching. Graph streams. ](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture4.pdf)
  * Lecture 5. [Linear algebra, dimensionality reduction](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture5.pdf)
  * Lecture 6. [Managing time change in data streams](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture6.pdf)
  * Lecture 7. [Data Stream Mining. Building decision trees](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture7.pdf)
  * Lecture 8. [Evaluation. More predictors. Clustering](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture8.pdf)
  * Lecture 9. [Frequent pattern mining in data streams](http://www.cs.upc.edu/~gavalda/DataStreamSeminar/files/Lecture9.pdf)

## Papers (grouped using the lectures above):

### The data stream model. Counting. Probability tools:
* The original Morris77 paper: http://dl.acm.org/citation.cfm?id=359627, also available here: http://www.inf.ed.ac.uk/teaching/courses/exc/reading/morris.pdf
* An analysis of Morris' counter, by Flajolet: http://algo.inria.fr/flajolet/Publications/Flajolet85c.pdf
* The application of Morris' counters to counting n-grams, by Van Durme and Lall: http://www.cs.jhu.edu/~vandurme/papers/VanDurmeLallIJCAI09.pdf
* (math intensive) Two explanations of large deviation bounds that I like, by A. Sinclair http://www.cs.berkeley.edu/~sinclair/cs271/n13.pdf and by G. Lugosi http://www.econ.upf.edu/~lugosi/anu.pdf

### Frequency problems:
* Noga Alon, Yossi Matias, Mario Szegedy: The space complexity of approximating frequency moments. J. Comput. Syst. Sci. 58(1): 137-147 (1999). Conference version, Symp. on the Theory of Computing (STOC) 1996.
* Piotr Indyk, David P. Woodruff: Optimal approximations of the frequency moments of data streams. STOC 2005: 202-208. The paper concentrates on proving lower bounds, which is out of the scope of this course. 
* general discussion on disctint element counting: http://highscalability.com/blog/2012/4/5/big-data-counting-how-to-count-a-billion-distinct-objects-us.html
* K.Y. Whang, B. Vander-Zanden, H.M. Taylor,  A Linear-time Probabilistic Counting Algorithm for Database Applications.  ACM Trans. Database Syst., 15:2, 1990.
* Edith Cohen, Size-Estimation Framework with Applications to Transitive Closure and Reachability . FOCS 1994 and JCSS 1997.
* The flajolet-martin probabilistic counter. Philippe Flajolet, G. Nigel Martin: Probabilistic Counting Algorithms for Data Base Applications. J. Comput. Syst. Sci. 31(2): 182-209 (1985). See also http://en.wikipedia.org/wiki/Flajolet-Martin_algorithm
* Durand, M.; Flajolet, P. (2003). "Loglog Counting of Large Cardinalities". Algorithms - ESA 2003. Lecture Notes in Computer Science 2832. p. 605. 
* Flajolet, P.; Fusy, E.; Gandouet, O.; Meunier, F. (2007). "HyperLogLog: the analysis of a near-optimal cardinality estimation algorithm". AOFA ’07: Proceedings of the 2007 International Conference on the Analysis of Algorithms.
* Flajolet's contributions explained beautifully by J. Lumbroso: http://www.stat.purdue.edu/~mdw/ChapterIntroductions/ApproxCountingLumbroso.pdf
* Kane, Nelson, Woodruff. An Optimal Algorithm for the Distinct Elements Problem. Principles of Database Systems (PODS) 2010
* For more on HyperLogLog and the graph neighborhood estimation:
  * http://en.wikipedia.org/wiki/HyperLogLog
  * http://research.neustar.biz/2012/10/25/sketch-of-the-day-hyperloglog-cornerstone-of-a-big-data-infrastructure/
* A live demo of hyperloglog at the web above: http://content.research.neustar.biz/blog/hll.html
* http://www.slideshare.net/sunnyujjawal/hyperloglog-in-practice-algorithmic-engineering-of-a-state-of-the-art-cardinality-estimation-algorithm
* http://stackoverflow.com/questions/12327004/how-does-the-hyperloglog-algorithm-work
*optimizations that I'd like to try: http://druid.io/blog/2014/02/18/hyperloglog-optimizations-for-real-world-systems.html
* more optimizations: http://research.google.com/pubs/pub40671.html

## Sampling. Finding frequent elements. The CM-sketch:
J. Vitter. Random Sampling with a reservoir.  ACM Trans. on Mathematical Software, 1985.
Good survey of heavy hitter algorithms. Radu Berinde, Graham Cormode, Piotr Indyk, Martin J. Strauss. Space-optimal Heavy Hitters with Strong Error Bounds
 Also very good survey: Graham Cormode, Marios Hadjieleftheriou. Finding Frequent Items in Data Streams. Proc. VLDB Endowment, 2008
Richard M. Karp, Scott Shenker, Christos H. Papadimitriou. A Simple Algorithm for Finding Frequent Elements in Streams and Bags. ACM Transactions on Database Systems (TODS), Volume 28, 2003.
The Space-Saving sketch paper. Ahmed Metwally, Divyakant Agrawal, Amr El Abbadi. Efficient Computation of Frequent and Top-k Elements in Data Streams. Intl. Conf. on Database Technology (ICDT) 2005.
M. Charikar, K. Chen and M. Farach-Colton. "Finding Frequent Items in Data Streams." ICALP 2002 (conf. version) and Theoretical Computer Science 2004 (journal version)
The CM-Sketch paper. Graham Cormode and S. Muthukrishnan: An improved data stream summary: The Count-min sketch and its applications.  J. Algorithms 55: 29–38
On Frugal Streaming, a neat sketch for estimating quantiles which I did not cover in the course: http://research.neustar.biz/2013/09/16/sketch-of-the-day-frugal-streaming/
And more on the CM-sketch
http://en.wikipedia.org/wiki/Count-min_sketch 
https://sites.google.com/site/countminsketch/
https://tech.shareaholic.com/2012/12/03/the-count-min-sketch-how-to-count-over-large-keyspaces-when-about-right-is-good-enough/


## Lecture 4:
Discussions on sketch merging are a bit all over. This is sort of an overview.
Christopher R. Palmer, Phillip B. Gibbons and Christos Faloutsos, ANF: A Fast and Scalable Tool for Data Mining in Massive Graphs,  KDD 2002.
Paolo Boldi, Marco Rosa, and Sebastiano Vigna. HyperANF: Approximating the neighbourhood function of very large graphs on a budget. WWW, 2011.
Lars Backstrom, Paolo Boldi, Marco Rosa, Johan Ugander, Sebastiano Vigna. Four Degrees of Separation. ACM Web Science 2012, 2012.
A survey on streaming graph algorithms: http://people.cs.umass.edu/~mcgregor/papers/13-graphsurvey.pdf
