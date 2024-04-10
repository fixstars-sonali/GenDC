if not get_option('tests').disabled()
  if host_machine.system() == 'linux'  and gstcheck_dep.found()
    subdir('check')
  else
    subdir('check')
  endif

endif

## TODO
# if not get_option('examples').disabled()
#   subdir('examples')
# endif
