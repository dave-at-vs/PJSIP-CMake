file(GLOB_RECURSE SPEEX_SRC ../../speex/libspeex/*.h config.h)
set(SPEEX_SRC ${SPEEX_SRC}
  ../../speex/libspeex/bits.c
  ../../speex/libspeex/buffer.c
  ../../speex/libspeex/cb_search.c
  ../../speex/libspeex/exc_10_16_table.c
  ../../speex/libspeex/exc_10_32_table.c
  ../../speex/libspeex/exc_20_32_table.c
  ../../speex/libspeex/exc_5_256_table.c
  ../../speex/libspeex/exc_5_64_table.c
  ../../speex/libspeex/exc_8_128_table.c
  ../../speex/libspeex/fftwrap.c
  ../../speex/libspeex/filterbank.c
  ../../speex/libspeex/filters.c
  ../../speex/libspeex/gain_table.c
  ../../speex/libspeex/gain_table_lbr.c
  ../../speex/libspeex/hexc_10_32_table.c
  ../../speex/libspeex/hexc_table.c
  ../../speex/libspeex/high_lsp_tables.c
  ../../speex/libspeex/jitter.c
  ../../speex/libspeex/kiss_fft.c
  ../../speex/libspeex/kiss_fftr.c
  ../../speex/libspeex/lpc.c
  ../../speex/libspeex/lsp.c
  ../../speex/libspeex/lsp_tables_nb.c
  ../../speex/libspeex/ltp.c
  ../../speex/libspeex/mdf.c
  ../../speex/libspeex/modes.c
  ../../speex/libspeex/modes_wb.c
  ../../speex/libspeex/nb_celp.c
  ../../speex/libspeex/preprocess.c
  ../../speex/libspeex/quant_lsp.c
  ../../speex/libspeex/resample.c
  ../../speex/libspeex/sb_celp.c
  ../../speex/libspeex/scal.c
  ../../speex/libspeex/smallft.c
  ../../speex/libspeex/speex.c
  ../../speex/libspeex/speex_callbacks.c
  ../../speex/libspeex/speex_header.c
  ../../speex/libspeex/stereo.c
  ../../speex/libspeex/vbr.c
  ../../speex/libspeex/vorbis_psy.c
  ../../speex/libspeex/vq.c
  ../../speex/libspeex/window.c)

include_directories(AFTER SYSTEM  . ../../speex/include/)

add_definitions(-DHAVE_CONFIG_H -D_USE_MATH_DEFINES)

add_library(speex OBJECT ${SPEEX_SRC})
