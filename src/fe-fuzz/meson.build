# this file is part of irssi

subdir('irc')
subdir('fe-common')

executable('irssi-fuzz',
  files(
    'irssi.c',
    '../fe-text/module-formats.c',
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

executable('server-fuzz',
  files(
    'server.c',
    '../fe-text/module-formats.c',
  ),
  link_with : [
    libconfig_a,
    libcore_a,
    libfuzzer_fe_common_core_a,
    libirc_a,
    libfe_common_irc_a,
    libfe_irc_dcc_a,
    libfe_irc_notifylist_a,
  ],
  link_args : [fuzzer_lib],
  include_directories : rootinc,
  implicit_include_directories : false,
  install : true,
  dependencies : dep
)

# noinst_headers = files(
#   '../fe-text/module-formats.h',
# )
