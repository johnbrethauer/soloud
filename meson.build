project('soloud', 'c', 'cpp')

r = run_command('src.sh')
soloud_src = r.stdout().strip().split('\n')
soloud_inc = include_directories('include')
add_project_arguments('-DWITH_MINIAUDIO', language:'cpp')

soloud_lib = library('soloud',
  sources: soloud_src,
  include_directories: [soloud_inc]
)

soloud_dep = declare_dependency(
  link_with: soloud_lib,
  include_directories : soloud_inc
)