# Alternatives to Makefiles

I am unsure if like or dislike Makefiles.

Building software with Makefiles works.

# Missing features

## Missing: Short cut other than "mtime of file A is younger than mtime of file B"

If I look at this:

```
mytarget:
    if [ $(shell some_command) = "skip" ]; then \
        echo "Skipping mytarget"; \
    else \
        echo "Executing mytarget"; \
        # add your commands here \
    fi
```

... then I think it would be better to switch from Makefile to bash scripts.

# Requirements

## Local builds

Builds should run locally without internet connection.

# Alternatives

https://github.com/earthly/earthly

https://github.com/nektos/act 


#
