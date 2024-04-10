
gendcparse_src = [
  'gstgendcseparator.c',
]

gendcparse_headers = [
  'gstgendcseparator.h',
]

# gendc_dep = declare_dependency(link_with : gendc,
#   include_directories : [include, separator]
#   )

gstgendcseparator = library('gstgendcseparator',
  gendcparse_src,gendcparse_headers,
  c_args : gst_plugins_args,
  include_directories : [include,configinc, separator],
  dependencies : [gstbase_dep,gendc_dep],
  install : true,
  install_dir : plugins_install_dir,
)
plugins += [gstgendcseparator]