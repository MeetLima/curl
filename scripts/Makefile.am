ZSH_FUNCTIONS_DIR = @ZSH_FUNCTIONS_DIR@
PERL = @PERL@

ZSH_COMPLETION_FUNCTION_FILENAME = _curl

all-local: $(ZSH_COMPLETION_FUNCTION_FILENAME)

$(ZSH_COMPLETION_FUNCTION_FILENAME): zsh.pl
	$(PERL) $< > $@

install-data-local:
	$(MKDIR_P) $(DESTDIR)$(ZSH_FUNCTIONS_DIR)
	$(INSTALL_DATA) $(ZSH_COMPLETION_FUNCTION_FILENAME) $(DESTDIR)$(ZSH_FUNCTIONS_DIR)/$(ZSH_COMPLETION_FUNCTION_FILENAME)