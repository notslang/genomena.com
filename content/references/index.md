---
publish-date: '2013-09-26T15:44:00'
tags: 'Genetics, evolution, and policy'
---

# Three small steps toward genomically sensible healthcare

![Sailing a close reach, San Francisco Bay. (Image copyright Nathaniel Pearson)](/wp-content/uploads/2013/08/Sailing-1024x625.jpg)

Sailing a close reach, San Francisco Bay. (Image copyright Nathaniel Pearson)

[A talk](http://www.slideshare.net/NathanielPearson/pearsontcgc2013) at [the Clinical Genome Conference](http://www.clinicalgenomeconference.com/) resonated with some folks, who suggested sharing it. Crucially, that crowd included doctors, who have much to both teach and learn in the brave new world of genomic medicine. With them on hand, the day's session loosely echoed a [grand rounds](http://en.wikipedia.org/wiki/Grand_rounds), where the case was, soberingly, the tall order of making genomes widely useful in healthcare.

In such circles, a genomicist like me is a narrow specialist. Bigger speakers -- general practitioners, so to speak -- were lined up to cover the chronic, integrative needs on the [conference bingo](http://www.sciencenews.org/view/generic/id/346343/description/Buzzword_bingo) card: _convening stakeholders_; _establishing standards for reporting and payment_; _managing big data_...a wordsquall that looms over our field, [easy to discuss](http://quoteinvestigator.com/2010/04/23/everybody-talks-about-the-weather/) but hard to fix.

So rather than tackle such broad challenges, my talk stayed bite-size. Building from insights on genome structure, function, and variation, it urged three small but concrete ways to help put genome-informed healthcare on firmer footing.

- Use different reference genomes to align a person's raw data (pick reference(s) most like her/him) versus store her/his finished genome (as clear or potential differences from the _human ancestral reference_).
- Clinically classify _genotypes_, not variants.
- Filter a genome against other _individuated genomes_, not allele frequency tables.

Though these ideas aren't new, they would break convention -- so need justifying. But even if you skip the explanations that follow (starting with this post), know that the proposals reflect long thought on how current convention, rooted in sparse data, will ultimately fail for millions of whole human genomes. Thus consider them early course tweaks that can save bigger tacks later, en route to genomically informed healthcare for all of us.

## Small step I: The right reference genome(s)

A reference genome -- we'll just say _reference_ -- is a long string of letters used as a common template for comparing the genomes of closely related organisms, such as people. As an archetype, a reference often shortens and simplifies real genomes,[1] to help _read_, _write_, or _interpret_ them.

In teasing apart these tasks, note that today we use the same human reference for all three...and that it's right for none of them. Below we'll see why, and what we should do about it. But if you're rushed, here's the gist:

_The current single reference is arbitrary and ethnocentric; inevitably misaligns most people's raw data; and is poor for writing and interpreting genomes afterward, because it includes rare and risky variants, and muddles summary insights on data quality and evolution._

An alternative made of just common or putatively healthy variants would still be unreliable for aligning raw data, and as a foil for writing and interpreting genomes.

Instead, we should read your genome by aligning raw data to references most like you (we can usually guess which). We should then write all our genomes against the human ancestral reference -- a solution that's ethnically neutral, directly informative on data quality and evolution, and stabler than alternatives.

And we should give up on using any reference to proxy an idealized healthy genome. As later posts will detail, reliable health insight will instead require comparing your genome to the individuated whole genomes of many other people who, like each of us, get some diseases and not others.

Ok, now let's walk through those reference tasks in detail, to better understand why we must do them differently.

## Read

To read your genome -- that is, to make out the long eye chart of letters that form it -- a modern sequencer streams zillions of DNA snippets, each copying a chromosome tract roughly at random. By comparing each snippet to a good reference, a computer can find where it best fits, much as we match jigsaw puzzle pieces to the picture on the box. As snippets pile up, the computer surveys what DNA letter(s) amass over each spot, to guess what letter(s) your chromosomes carry there.[2] Conventionally, we've taken a one-size-fits-all approach to this task of _aligning_ snippets, using the same reference, called _Hg#_ (where today # = [19](http://hgdownload.cse.ucsc.edu/goldenPath/hg19/bigZips/)), to scaffold everyone's genomes.[3] But Hg# wasn't carved in stone. Instead, it's quilted from [several real people](http://seqanswers.com/forums/archive/index.php/t-22278.html)'s genomes that were read by costly, reference-free methods. And the haphazardly picked people who contributed to it have their own ancestry, which gives Hg# their genetic quirks.

As a result, some human genomes are more like Hg# than others. And if my genome resembles it more than yours does, my snippets will, on average, align more reliably. Conversely, because [big populations tend to be genetically diverse](/ne/), Hg# -- like _any_ single option -- inevitably misaligns raw data from _most_ people's genomes, in ways both big (mutual gaps and rearrangements wreak havoc) and small (clustered small differences leave good snippets unaligned).

In the end, this means that _we can best read your genome today by first aligning to the available genome(s) most like it._[4] Happily, [skimming](http://en.wikipedia.org/wiki/SNP_array) your genome -- or even just looking at you -- strongly hints whose genome(s) might work best.[5] How well we can play reference sommelier depends on what options are on hand (more and more, starting with [synthetic references](http://www.plosgenetics.org/article/info%3Adoi%2F10.1371%2Fjournal.pgen.1002280) that proxy what's common in a particular part of the world), and how saliently _mixed_ your recent ancestry is. But if needed we can try _multiple_ references, and see which work best for which snippets.

And that raises two deeper points. First, for some genome segments, such as a [stunningly diverse and health-relevant stretch of chromosome 6](http://en.wikipedia.org/wiki/Human_leukocyte_antigen), it's hard to predict what your genome looks like _regardless_ of where your forebears came from. For such segments, it makes sense to _always_ align your snippets to many reference options.[6] Doing so takes a few more electrons, but usefully sharpens the resulting picture of your genome.

Second, aligning your snippets to even one whole _real_ genome would itself be like aligning them to _two_ versions of a conventional reference (with its one copy of each chromosome that's paired in real genomes). Smartly, that could fully leverage new algorithms that track _everywhere_ a snippet decently fits during alignment, rather than just picking one spot (often by tossup). And that, in turn, would let us read your genome more finely, without -- yet -- needing the compact simplicity of a conventional reference like Hg#.

Which brings us to the next use of a reference...

## Write

After we read your genome in detail, a reference helps _write_ it. Namely, because copies of a given human chromosome are all grossly alike, we can thriftily store yours by just noting where one or both mismatch a simple (single-copy) reference, or were read too poorly to tell.

Everywhere else -- typically, >95% of the currently sequenceable parts of human chromosomes -- we can assume that your copies match that reference. And because many of your poorly read sites will themselves clump in compressible tracts, we can shrink your genome >>20-fold in the end. That saves memory, of course, but also helps us query it -- most usefully, by comparing your DNA (plus your phenotypes, ideally) to others'.

But there's a catch. Because mutation anywhere on a chromosome can make one copy of it _longer_ than another, genomes can best be compared if stored as differences from the same reference, so their mapping coordinates match. That way, like sailors agreeing to [track longitude from Greenwich](http://en.wikipedia.org/wiki/Prime_meridian), we can neatly record findings like _'One of your chromosome 7′s shows five more bases (ACGTA) than mine at reference site 1000; but one of mine shows three fewer bases at reference sites 2000-2002_'...

Note the dilemma here: to read genomes, we should align their snippets to _various_ most-appropriate real reference(s); but to compare them, we should write them as differences from the _same_ simple reference.[7] Bottom line, we need task-specific references.

But that still means picking one best reference for writing genomes. Given that so much work has gone into Hg#, we might ask whether _it's_ the right one. Which leads us to the third use of references...

## Interpret

After shrinking your genome to a list of differences from a reference, we'd like to understand that list -- what it says about how sequencing went and, more importantly, about you. We might even hope to use the reference to proxy a _healthy_ genome, so that anything worrisome in your genome stands out from it.

Alas Hg# makes a poor interpretive foil for real genome data, starting with quality control: because Hg# comes from a few modern people, it's poor not just for aligning, but also for writing, where it can conflate statistical signatures of lab-bench problems (sample contamination, chemistry failure, &c.) with those of ancestry. QC that first compares _heterozygosity_ of particular genome segments, rather than just counting reference sites called with any mismatch, will help there (an issue for another day...), but the problems with the current reference go deeper.

In particular, Hg# also includes many variants already [implicated in diseases](http://www.ncbi.nlm.nih.gov/pubmed/21121051) -- which means it won't always flag your own worrisome DNA spellings[8] , and that it troublesomely differs from some [single-gene references](http://www.lrg-sequence.org/) familiar to clinical geneticists. Moreover, Hg# includes many other variants that, while not yet well studied, are [suspiciously rare](/rare-variants-and-health/) enough to be harmful too.

Given those shortcomings, many have suggested replacing Hg#'s rare and/or known risky variants with common and/or healthy alternatives, ostensibly yielding a new reference that reliably proxies a healthy, normal genome.

Alas, that won't work, for two reasons. _What's common varies. And what's healthy depends._

## Informative beats (un)healthy

At first glance, one of your DNA spelling variants may be rare enough on earth overall to intrigue us -- but turn out to be boringly common among millions of mostly healthy people in some small patch of the planet. More profoundly, the commonest variant at a genomic site today or in five years may not be the commonest one next year or in ten years. That's evolution -- and it means that a common-only reference is inherently unstable.

On the health side, meanwhile, many variants aren't simply good or bad. Their effects depend on what how many copies you have (0, 1, or 2), what disease we ask about, and what _other_ variants lurk in your genome.

You may know a few such twists already. _One or two copies of T [here](http://genome.ucsc.edu/cgi-bin/hgTracks?position=chr11:5247982-5248482&hgsid=345050099&snp137Common=pack&hgFind.matches=rs334,) help avoid malaria and high cholesterol -- but two copies leave you with crippling anemia. One copy of A over [there](http://genome.ucsc.edu/cgi-bin/hgTracks?hgHubConnect.destUrl=..%2Fcgi-bin%2FhgTracks&clade=mammal&org=Human&db=hg19&position=chr17%3A41243941&hgt.positionInput=chr17%3A41243941&hgt.suggestTrack=knownGene&Submit=submit&hgsid=345051025) can drive breast cancer, but mainly if you also lack a working copy of the [SRY](http://en.wikipedia.org/wiki/SRY) gene (which, on the flipside, helps you avoid testicular cancer, among other diseases...)._ And so forth.

Data from millions of us will unfurl more astounding complexity, where variants throughout your genome -- some inevitably present in any reference we use -- interact in surprising ways with each other, and with habits and other factors, to favor some diseases and disfavor others.[9] Other posts will further explore how this hard truth should alter our approach to genomic healthcare. Here, it simply dooms any hope of using any reference to reliably proxy what's healthy.

And more deeply, using a reference like Hg# as an interpretive yardstick also obscures how genomes change and, by extension, how various kinds of changes tend to affect health in the first place. Hg# can't, for example, tell us whether a so-called _deletion_ in your genome (where it's missing a tract found in Hg#) really reflects a mutation that deleted bases in you or your forebear, or instead reflects an _insertion_ of bases in someone who contributed to Hg#.

As such, because a given letter in a reference like Hg# could itself reflect a past mutation, writing _everyone's_ genomes as differences from Hg# makes statistical questions like _'How often does the snippet CG mutate to TG? And how well does that TG survive, over generations, if it changed a protein's arginine to cysteine?'_ trickier than they should be.

Such questions matter. They can unlock basic physiology (_How do mutations happen? Why do tumors correct them so poorly?_); hint how a new variant may affect health (_Does changing active-site arginine to cysteine often make an enzyme fail?_); and clarify how variants _interact_ with each other, and with habits, to cause disease (_Why do some genetic variants, like [APOE-ε4](http://snpedia.com/index.php/ApoE-%CE%B54), make us sick but leave chimpanzees healthy?_).

Those big questions require the big data inside us. Even if no more than a handful of your DNA spellings alter your own healthcare, the rest of them, pooled with similar data from all of us, can shed light on many diseases to greatly refine care for our grandkids.

But using a conventional reference like Hg# needlessly hinders that effort. So while we must abandon the idea of any reference reliably proxying a healthy genome, can we at least find a sensible reference to write and compare the coming flood of genomes, to catalyze those deeper insights?

## An ancestral reference

We can. The sensible yardstick for writing your genome is the _human ancestral reference_ (_HAR_) -- that is, a single-copy genome comprising, at each chromosomal site, the DNA letter carried by the last common ancestor of all people for that site.

In picturing the HAR (which [Suganthi Balasubramanian](https//twitter.com/suganthibala) and colleagues have already [described here)](http://genesdev.cshlp.org/content/25/1/1.long)[10] , note something very important: two genomic sites, even on the same chromosome, can trace to _different_ last common ancestors. That's because, when eggs and sperm are made, chromosomes pair up, swap segments, and move into different cells. Each copy of a chromosome thus quilts together pieces of earlier copies; so everyone's last common ancestor for site 1000 may not be our last common ancestor for site 1001 (they may have even lived eons apart). Which also means it's implausible that any person ever carried the whole HAR.[11] Among reference options for writing and comparing our genomes, the HAR uniquely combines several appealing features:

- _It's neutral._ As noted, no one ever carried the whole HAR. And because the mutations that distinguish our genomes from it have struck roughly randomly among our ancestors, your genome resembles it about as much as mine does.[12]

  In this important sense, the HAR belongs to none of us, and to all of us. Being roughly equidistant from everyone, it offers a uniform, non-ethnocentric baseline for assessing sequencing quality, and for reporting what's genetically distinctive about you.

- _It's stable._ The HAR actually looks a lot like a common-variants-only reference, because nearly all ancestral variants are common. But while a common-only reference would in principle need many edits each year to stay perfectly accurate, the HAR would need just a few (as atypically rare ancestral variants are newly found or, occasionally, learned to have gone extinct).[13]

  Such editing isn't urgent, because few variants with allele frequency near 50% are functionally intriguing enough, or surveyed precisely enough in the population, to day-trade anyway. But that just makes it even smarter to build a reference on the stable, reliably inferrable, and meaningful criterion that a variant be ancestral, rather than worry whether its allele frequency fell to 49.9%. That way, we get summary insights even from otherwise boring variants -- and a low-maintenance reference to boot.

- _It's compact but comprehensive._ Like conventional references, the HAR is a simple single-copy (_haploid_) genome. Real genomes, compressed against it, would yield files consistently intermediate in size between the biggest and smallest files compressed against Hg#.[14]

  Nonetheless, because new chunks of DNA are usually copied from chunks elsewhere in the same genome, the HAR includes source DNA for nearly all chunks of real human genomes (missing only those recently copied from viruses or bacteria, or other oddities). Other reference options tend to be less comprehensive on these counts, which poses an ongoing dilemma of when to add a segmental copy (to make them more thorough), versus omit it (to keep them compact).[15]

  That dilemma would still hold, but the HAR offers a framework for handling extra segments that we choose to include in the _extended_ HAR that [Subramanian _et al._ proposed](http://genesdev.cshlp.org/content/25/1/1.long). For a newly arisen extra segment that some but not all people have, variation _among_ such copies could in turn be mapped to common coordinates in the inferred earliest (nearest to universally ancestral) version of the new copy.

- _It's directly informative._ Most importantly, the HAR is the only reference option that directly shows how human genomes change. As a foil for writing all our genomes, it would thus most quickly reveal summary patterns of change that in turn shed light on basic biology and health.As a concrete example, if shortening a particular bend shared by a particular family of proteins makes people sick, but lengthening it -- or shortening another bend -- leaves people healthy, the HAR would let clinical geneticists reliably spot this trend faster than other references would.

The benefits of an ancestral reference for making sense of genomes, both individually and together, have long been starkly clear for geneticists studying the first fully sequenced human chromosome: the mitochondrial genome (mtDNA).

Starting in 1981, we used the [first sequence of a person's mtDNA](http://www.ncbi.nlm.nih.gov/pubmed/7219534) as a reference. That sequence forms a leaf on the [simple evolutionary tree](http://www.phylotree.org/tree/main.htm) that binds all our mtDNA versions. And because each of us gets only our mom's version of this short but gene-rich chromosome, with no backup from dad, that tree's branches are key foci of health research.

But using a modern person's mtDNA as a reference meant treating a leaf as if it were the treetrunk. This everted our view of the tree, prompting [epicycle](http://www.dailymotion.com/video/xerwsh_carl-sagan-videos-epicycles-of-ptol_tech)-like contortions to figure out where your leaf was, and how your branch may or may not have mutated in telling ways.

In 2012, researchers cut that gordian knot, proposing the [human ancestral mtDNA](http://www.mtdnacommunity.org/) as a reference for writing real genomes. That new reference lets you easily a) find your mtDNA leaf, and b) see how DNA has changed throughout the tree, to better understand key biological processes.

Having learned the hard way with mtDNA, we needn't wait 31 years for our other chromosomes. In the end, by using multiple references to align raw data, and adopting the HAR to write and compare our finished genomes, we can best read, write, and learn from the millions of human genomes soon to be sequenced.

## Getting smarter with references

So where are we, as a community, on human reference genomes?

There's modest reason to hope. Researchers have begun to show how much better we might read genomes by [aligning snippets to similar reference(s)](http://www.plosgenetics.org/article/info:doi%2F10.1371%2Fjournal.pgen.1002280); that an [ancestral reference helps](http://genesdev.cshlp.org/content/25/1/1.long) compare genomes [more easily and informatively](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3322232/); that [Hg# doesn't proxy a healthy genome](http://www.ncbi.nlm.nih.gov/pmc/articles/pmid/21121051/); and that [no alternative would reliably do so](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3254080/) either.

On the practical side, we're accumulating diverse, ever better sequenced human genomes that can serve well as alignment references (and, as a bonus, help [benchmark new sequencing methods](http://www.nist.gov/mml/bbd/biomolecular/genome_in_a_bottle_consortium.cfm)). And we're getting better genomes from elsewhere in the great ape family tree, to refine the HAR.

Moreover, today's _de facto_ standard, Hg#, continues to improve via thoughtful work by [Deanna Church](http://infocus.nlm.nih.gov/2012/08/meet-ncbis-deanna-church-genom.html)'s team and [others](http://www.ncbi.nlm.nih.gov/pubmed/23932108). Beyond fixing errors and filling in previously missing segments, the pending Hg20 version will include _multiple_ versions of more segments, in part to better align raw data.

That's a sensible stopgap, until more folks start picking from multiple alignment references from the start. But adding alternate versions of more segments to Hg# requires ongoing arbitrary choices, slows the task of writing finished genomes, and tends to statistically weaken comparisons of many genomes. The latter jobs are really better served by writing genomes against the HAR.

Communal habits like using Hg# for all human reference needs are hard to break -- even for open-minded scientists (and maybe moreso in famously stubborn medicine). But given the clear flaws in our current approach to reference genomes, it's likely better to break those bad habits now than let them entrench further, as we start sequencing patients' genomes by the thousands (and more).

Making all those genomes useful in healthcare, for us and future generations, will mean reading them well; writing them efficiently; and, as coming posts will explore further, interpreting them wisely.

All these goals rest on the bedrock of reference genomes. Let's get them right.

[^l] Today's ~2.9 billion-letter [human reference](http://genome.ucsc.edu/cgi-bin/hgTracks), for example, comprises just one version of each of the grossly distinct-looking molecules (chromosomes 1-22, X, Y, and M) in the >6.5 billion-letter genome of a man's skin cell. That cell's genome comprises _two_ copies of most such chromosomes -- and those copies, in turn, differ in chemical makeup (base sequence), and include tracts that have never been seen (or successfully sequenced), so are simply missing from the reference.

[^2] Importantly, many snippets from your genome differ from even their best-matching parts of the puzzlebox picture (otherwise, why bother sequencing?). But the reference template still helps piece them together faster than we otherwise could. And by piling _many_ snippets over each site, we can tune out errors from cooking finicky chemicals under tiny image sensors -- a bit like how astronomers, at the other end of the spatial scale, distinguish lasting light sources from noise by overlaying many pictures of the same part of the sky.

[^3] While researchers colloquially use the _Hg_ prefix, this technically denotes the version stored at the University of California Santa Cruz's popular [genome data portal](http://genome.ucsc.edu/); the current reference's proper name is *GRCh##.p__, where ## (currently 37) is a _major assembly release* number higher than the # in Hg#, and *is a _patch release* number.

[^4] That point was moot in 2003, when we had to use the hardwon sequence that became the current reference. But since then, we're bootstrapping our way to good sequences of _many_ human genomes from around the world -- a pool that we should tap to better align newly sequenced genomes, as some folks have already shown.

[^5] Ideally, we'd use parents' genomes to align those of their kids...but when sequencing is common enough to make that practical, sequencers will likely make longer snippets that are easier to piece together from the start anyway, even without aligning to a reference.

[^6] Helpfully, Hg# itself includes several options for some such segments -- and those who built and refine it plan to add more.

[^7] Note that even though we write them as differences from a simple reference, which has just one copy of each chromosome, we can still readily encode which spellings go _together_ on each copy of your chromosomes (if our sequencing method was good enough to tell in the first place).

[^8] Especially if whoever compressed your genome didn't bother noting where your genome was too poorly sequenced to know what it carries -- a corner that geneticists too often cut.

[^9] Such insights stand to turn much of the noise that we currently sweep under the rug of _partial penetrance_ into far better understood signal -- think, for example, about how genetic insight turned the apparent random noise of why a baby was born female or male into causal signal tracing largely to the sex chromosomes.

[^10] For the remaining sites, we can't reliably guess what variant our last common ancestor carried, because the state of variation we see among our copies extends to other great apes, suggesting that such variation has either arisen twice, or lasted too long to reliably unravel. In extreme cases, like the sex chromosomes, such lasting variation is already enshrined in the current reference (Hg# has one X sequence and one Y sequence, despite the fact that not everyone has the latter).

[^11] Even the last common ancestors who contributed to the HAR had variants in their own genomes that aren't in it.

[^12] Planetwide, we have no idea whose genome happens to differ from it most, though that person -- ironically, in some sense the most evolved (geneticists would say _derived_) of us -- is almost certainly very sick, thanks to gross genetic changes...

[^13] Many thanks to [Graham Coop](http://gcbias.org/) and [Justin Fay](http://www.genetics.wustl.edu/jflab/) for helping think through the relevant numbers here.

[^14] Average compression is the main measure that could instead be optimized by a common-only reference. But the HAR has several substantive advantages over that less stable and informative option.

[^15] Note, btw, that this question matters most if we're using a reference to align snippets -- which we're not proposing here. But we do need to map each of the alignment references themselves to the writing/comparing reference, which is where it helps to make sure the latter includes source DNA for the segments that those alignment references may have extra or fewer copies of.
