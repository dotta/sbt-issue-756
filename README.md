sbt-issue-756
=============

Sample project that demonstrates sbt issue #756

Looks like (Java?) annotations are not correctly tracked by sbt incremental compiler. In fact, when changing the name of a class 
that is referenced in annotation of a Java class, sbt should fail compilation, because the referenced class name no longer exist. 
However, compilation works just fine! To actually make compilation fail you need to get rid of the project's local .cache file.
