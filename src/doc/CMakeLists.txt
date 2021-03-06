# Aseprite Document Library
# Copyright (C) 2001-2016 David Capello

if(WIN32)
  add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

add_library(doc-lib
  algo.cpp
  algorithm/flip_image.cpp
  algorithm/floodfill.cpp
  algorithm/polygon.cpp
  algorithm/resize_image.cpp
  algorithm/rotate.cpp
  algorithm/rotsprite.cpp
  algorithm/shift_image.cpp
  algorithm/shrink_bounds.cpp
  anidir.cpp
  blend_funcs.cpp
  blend_mode.cpp
  brush.cpp
  brush_type.cpp
  cel.cpp
  cel_data.cpp
  cel_data_io.cpp
  cel_io.cpp
  cels_range.cpp
  compressed_image.cpp
  context.cpp
  conversion_she.cpp
  document.cpp
  documents.cpp
  file/col_file.cpp
  file/gpl_file.cpp
  file/hex_file.cpp
  file/pal_file.cpp
  frame_tag.cpp
  frame_tag_io.cpp
  frame_tags.cpp
  handle_anidir.cpp
  image.cpp
  image_impl.cpp
  image_io.cpp
  images_collector.cpp
  layer.cpp
  layer_io.cpp
  layer_list.cpp
  mask.cpp
  mask_boundaries.cpp
  mask_io.cpp
  object.cpp
  object.cpp
  palette.cpp
  palette_io.cpp
  primitives.cpp
  remap.cpp
  rgbmap.cpp
  selected_frames.cpp
  selected_layers.cpp
  site.cpp
  sort_palette.cpp
  sprite.cpp
  sprites.cpp
  string_io.cpp
  subobjects_io.cpp
  user_data_io.cpp)

# TODO Remove 'she' as dependency and move conversion_she.cpp/h files
#      to other library/layer (render-lib? new conversion-lib?)
target_link_libraries(doc-lib
  she
  gfx-lib
  fixmath-lib
  laf-base)
