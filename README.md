ouroboros
=========

*This is how the world stood still, when we climbed atop, and saw but all.*

 * Gather a directory of all R packages, e.g., from CRAN or by looking through Github.
   From the man pages, extract those functions that mention `predict`.

 * Since R is homoiconic, compute on the language! Execute each line in the example one by one, and
   carefully inspect the types of all expressions as well as the abstract syntax tree. These clues should
   be enough to make an earnest attempt at producing a Working Example.
   
   The idea is to create a homeomorphism
   from the initial example, which trains a model on a sample data set, to our data set. For example, we can
   look for data.frames of large sizes, and for response variables we can look to arguments to predict functions
   that are a numeric vector of the same length as the number of rows in the data.frame.

   This understanding can then be stitched into an ad lib syberia model, possibly with further experimentation to
   see which setups work and don't (e.g., discretizing all variables, etc.). For example, if the sample data set
   is all factors, we can assume discretization is important, and if the mean and standard deviation of the sample
   training set are 0 and 1, respectively, we can infer normalization is required.
  
 * As we iterate over every package looking for such examples, run models using Darwin. For models that fail
   across all permutation attempts, we simply error, and it becomes a human task to figure out the issue. 

 * The end result should be a "library" of generated tundra classifiers, together with potential data preparation
   guides. If Darwin has an automated validation system at this point, we can simply include these "modelettes"
   into our ensemble, with the correct permutation determined by cross-validation with many repetitions. Voila,
   the perfect ensemble! No package is left unturned, and the entire world lays bare.

NOTE: The above assumes the common sense principle that 80% of the value can be extracted from 20% the effort.
If most models are close to as good as they're going to get with out-of-the-box parameters (or "easy to find"
parameters), then this methodology should do incredibly well!
