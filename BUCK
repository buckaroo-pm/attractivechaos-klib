load('//:tests.bzl', 'createTests')
load('//:subdir_glob.bzl', 'subdir_glob')
load('//:buckaroo_macros.bzl', 'buckaroo_deps_from_package')

cxx_library(
  name = 'klib',
  header_namespace = '',
  srcs = glob(['*.c']),
  exported_headers = subdir_glob([
    ('','*.h')
  ]),
  visibility = [
    'PUBLIC',
  ],
  deps = buckaroo_deps_from_package('github.com/buckaroo-pm/host-pthread')
)

test_suite(
  name = 'test',
  tests = createTests(glob(['test/*_test.c']))
)
