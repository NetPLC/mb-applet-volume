pngs = mbvol-high.png mbvol-mid.png mbvol-low.png mbvol-zero.png 

EXTRA_DIST = $(pngs) mb-applet-volume.desktop TODO .autoipkg

INCLUDES = @APPLET_CFLAGS@			

bin_PROGRAMS = mb-applet-volume

mb_applet_volume_SOURCES = volume-applet.c			        

mb_applet_volume_LDADD = @APPLET_LIBS@ @MIXER_LIBS@

desktopdir = $(datadir)/applications/
pixmapsdir = $(datadir)/pixmaps/

pixmaps_DATA = $(pngs)

desktop_DATA = mb-applet-volume.desktop

