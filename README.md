# CS810-Fuzzware-CI
The demo of the Fuzzware CI project I made for my CS810 Final Class Project.

* the `fuzzbin/` directory contains relevant configuration files and the binary to be fuzzed. The files here are from the eample that Fuzzware provides.
* The fuzzing can be trigerred either manually or by making a pull request to this repo.
* By default, the fuzzing duration is set to 5 minutes. The default fuzzing duration can be changed with the FUZZ_DURATION repository variable in the format hh:mm:ss. This can go up to 6 days with the self hosted runner that is configured here. Manual triggers also give an option to override this duration, while pull requests always uses the setting in the repository variable if specified.

## Existing Pull Requests
For demonstration purposes, there are two dummy PRs that have had a fuzzing time of 10 minuted and 2 hours. The CI Action has added comments in each one summarizing the fuzzing results. They also include a link to download the zipped Fuzzware Project that you can download and inspect on your own machine.

## Trying It Out For Yourself!
I have set the FUZZ_DURATION to 2 mintues so you can quickly try out my project! 

Please make a dummy pull request to this repository. This could consist of an edit to this `README.md` file, or just adding a new file. Please do no modify anything under `fuzzbin/` or `.github`.

This should automatically trigget the Fuzzer action as a status check. Once the fuzzer is done, you should see a comment similar to the other pull requests get added. Again, you can use the link to download your fuzzware project to keep workign on it on your local machine. The project you download will contain plaintext/csv statistics at `fuzzware-project/stats/` that doesn't require Fuzzware on your local machine to study. If you have Fuzzware set up on your machine already, you should be able to replay runs too.

I will make sure that the self-hosted runner is running on my server until grades are posted on Workday. After that date, the server will be shut down.

Testing external pr...
