git-alias(1) -- Define, search and show aliases
===============================================

## SYNOPSIS

`git-alias` <br>
`git-alias` &lt;search-pattern&gt; <br>
`git-alias` &lt;alias-name&gt; &lt;command&gt; <br>
`git-alias` [--global] <br>
`git-alias` [--local] <br>
`git-alias` [--global] &lt;search-pattern&gt; <br>
`git-alias` [--local] &lt;search-pattern&gt; <br>
`git-alias` [--global] &lt;alias-name&gt; &lt;command&gt; <br>
`git-alias` [--local] &lt;alias-name&gt; &lt;command&gt; <br>

## DESCRIPTION

  List all aliases, show one alias, or set one (global or local) alias.

## OPTIONS

  --global

  Show or create alias in the system config

  --local

  Show or create alias in the repository config

  &lt;search-pattern&gt;

  The pattern used to search aliases.

  &lt;alias-name&gt;

  The name of the alias to create.

  &lt;command&gt;

  The command for which you are creating an alias.


## EXAMPLES

 Defining a new alias:

    $ git alias last "cat-file commit HEAD"

 Providing only one argument, `git-alias` searches for aliases matching the given value:

    $ git alias ^la
    last = cat-file commit HEAD

 `git-alias` will show all aliases if no argument is given:

    $ git alias
    s = status
    amend = commit --amend
    rank = shortlog -sn --no-merges
    whatis = show -s --pretty='tformat:%h (%s, %ad)' --date=short
    whois = !sh -c 'git log -i -1 --pretty="format:%an <%ae>

## AUTHOR

Written by Jonhnny Weslley &lt;<jw@jonhnnyweslley.net>&gt;

## REPORTING BUGS

&lt;<https://github.com/tj/git-extras/issues>&gt;

## SEE ALSO

&lt;<https://github.com/tj/git-extras>&gt;
