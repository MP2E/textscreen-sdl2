##-----------------------------------------------------------------------------
##
## Source Level CMake file.
##
##-----------------------------------------------------------------------------

include_directories(${CMAKE_SOURCE_DIR}/src ${CMAKE_SOURCE_DIR}/include ${SDL_INCLUDE_DIR})

add_library(textscreen
    textscreen.h
    txt_button.c
    txt_button.h
    txt_checkbox.c
    txt_checkbox.h
    txt_desktop.c
    txt_desktop.h
    txt_dropdown.c
    txt_dropdown.h
    txt_fileselect.c
    txt_fileselect.h
    txt_font.h
    txt_gui.c
    txt_gui.h
    txt_inputbox.c
    txt_inputbox.h
    txt_io.c
    txt_io.h
    txt_label.c
    txt_label.h
    txt_largefont.h
    txt_main.h
    txt_radiobutton.c
    txt_radiobutton.h
    txt_scrollpane.c
    txt_scrollpane.h
    txt_sdl.c
    txt_sdl.h
    txt_separator.c
    txt_separator.h
    txt_smallfont.h
    txt_spinctrl.c
    txt_spinctrl.h
    txt_strut.c
    txt_strut.h
    txt_table.c
    txt_table.h
    txt_utf8.c
    txt_utf8.h
    txt_widget.c
    txt_widget.h
    txt_window_action.c
    txt_window_action.h
    txt_window.c
    txt_window.h
    )

add_executable(calculator
    examples/calculator.c
    )

add_executable(guitest
    examples/guitest.c
    )

target_link_libraries(textscreen m)
target_link_libraries(calculator textscreen ${SDL_LIBRARY})
target_link_libraries(guitest textscreen ${SDL_LIBRARY})