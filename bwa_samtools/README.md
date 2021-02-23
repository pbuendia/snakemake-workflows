# Snakemake workflow: bwa_samtools

See https://github.com/snakemake-workflows/cookiecutter-snakemake-workflow

This is the BWA+Samtools Snakemake workflow. 
Insert your code into the respective folders, i.e. `scripts`, `rules`, and `envs`. Define the entry point of the workflow in the `Snakefile` and the main configuration in the `config.yaml` file.

## Authors

Patricia Buendia

## Usage

If you use this workflow in a paper, don't forget to give credits to the authors by citing the URL of this repository.


Activate the conda environment:

    conda activate snakemake

Test your configuration by performing a dry-run via

    snakemake --use-conda -n

Execute the workflow locally via

    snakemake --use-conda --cores $N

using `$N` cores or run it in a cluster environment via

    snakemake --use-conda --cluster qsub --jobs 100

or

    snakemake --use-conda --drmaa --jobs 100

If you not only want to fix the software stack but also the underlying OS, use

    snakemake --use-conda --use-singularity

in combination with any of the modes above.
See the [Snakemake documentation](https://snakemake.readthedocs.io/en/stable/executable.html) for further details.

### Investigate results

After successful execution, you can create a self-contained interactive HTML report with all results via:

    snakemake --report report.html

This report can, e.g., be forwarded to your collaborators.
An example (using some trivial test data) can be seen [here](https://cdn.rawgit.com/snakemake-workflows/rna-seq-kallisto-sleuth/master/.test/report.html).

### Commit changes

Whenever you change something, don't forget to commit the changes back to your github copy of the repository:

    git commit -a
    git push

### Obtain updates from upstream

If needed synchronize your workflow copy with new developments from upstream.



### Contribute back

In case you have also changed or added steps, please consider contributing them back to the original repository.



## Testing

Test cases are in the subfolder `.test`. They are automatically executed via continuous integration with [Github Actions](https://github.com/features/actions).

