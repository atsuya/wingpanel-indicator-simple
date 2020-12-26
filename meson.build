project(
    'simple',
    'vala', 'c',
    version: '2.1.7'
)

gettext_name = meson.project_name() + '-indicator'

prefix = get_option('prefix')
libdir = join_paths(prefix, get_option('libdir'))

add_global_arguments('-DGETTEXT_PACKAGE="@0@"'.format(gettext_name), language:'c')

wingpanel_dep = dependency('wingpanel-2.0', version: '>=2.1.0')
wingpanel_indicatorsdir = wingpanel_dep.get_pkgconfig_variable('indicatorsdir', define_variable: ['libdir', libdir])

shared_module('indicator-simple',
    'SimpleIndicator.vala',
    dependencies: wingpanel_dep,
    install: true,
    install_dir : wingpanel_indicatorsdir,
)
