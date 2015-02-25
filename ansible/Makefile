all_dirs = $(shell echo "roles/$(role)/{defaults,files,handlers,library,meta,tasks,templates,vars}")
main_dirs = $(shell echo "roles/$(role)/{defaults,handlers,meta,tasks,vars}")

role:
	@if [ "$($@)" = "" ]; then echo "Role is not defined. Pass -role=rolename"; exit 1; fi
	mkdir -p $(all_dirs)
	touch $(main_dirs)/main.yml

notes:
	-@find . -type f -name '*.yml' -exec fgrep -H -e TODO -e FIXME '{}' \;

.PHONY: notes role
