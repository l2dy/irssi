# this file is part of irssi
executable('theme-load-fuzz',
  files(
    'theme-load.c',
    '../../../fe-text/module-formats.c',
  ),
  link_with : [
    libconfig_a,
    libcore_a,
    libfuzzer_fe_common_core_a,
  ],
  link_args : [fuzzer_lib],
  include_directories : rootinc,
  implicit_include_directories : false,
  install : true,
  dependencies : dep
)

# noinst_headers = files(
#   '../../../fe-text/module-formats.h',
# )
