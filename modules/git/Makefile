GIT:= $(shell which git)

## Update submodules
git/submodules-update:
	$(call assert-set,GIT)
	$(GIT) submodule update --init --remote

## Update git aliases
git/aliases-update:
	@$(GIT) config --global --add alias.permission-reset '!git diff -p -R --no-color | grep -E "^(diff|(old|new) mode)" --color=never | git apply'

## Export git vars
git/export:
	@echo "GIT_COMMIT=$(GIT_COMMIT)"
	@echo "GIT_COMMIT_SHORT=$(GIT_COMMIT_SHORT)"
	@echo "GIT_BRANCH=$(GIT_BRANCH)"
	@echo "GIT_TAG=$(GIT_TAG)"
	@echo "GIT_IS_BRANCH=$(GIT_IS_BRANCH)"
	@echo "GIT_IS_TAG=$(GIT_IS_TAG)"
	@echo "GIT_TIMESTAMP=$(GIT_TIMESTAMP)"
