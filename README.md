<img src="https://raw.github.com/vizZ/bouncer/master/img/bouncer.png" width="250px" />

# Bouncer

Buncer is the big fat motherfucker standing in front of the motherfuckin' doorway of motherfuckin' stripclubs and keeps every motherfucker out if they are not on the motherfuckin' "list". So...
 
No motherfuckin' commit will ever enter the motherfuckin' stripclub if it breaks the motherfuckin' build or breaks the motherfuckin' tests. 

You go learn git, motherfucker!

### Usage

	> bouncer {start_commit} {end_commit} {path_to_verification_script} {optional_script_args}
	
The verification script has to retrun 0 if successful, otherwise the bouncer will stop.

This tool can be used as a post-push job on some CI server, like Bamboo, to verify integrity/purity of the branch (all commits have to pass the verification script).

When bauncer stops, you can fix your commit with `git commit --amend` or add a new commit and then rebase the whole branch with `git rebase --onto new_commit old_commit branch_ref`.

Good luck with the Bouncer...