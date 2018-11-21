# the SOURCE definiton lets move your makefile to another position
CONFIG 			= LIBRARY

# set pathes to the correct directories
SRC_DIR			= ../../../../source/Lib/TAppCommon
INC_DIR			= ../../../../source/Lib
LIB_DIR			= ../../../../lib
BIN_DIR			= ../../../../bin

SRC_DIR1		=
SRC_DIR2		=
SRC_DIR3		=
SRC_DIR4		=


USER_INC_DIRS	= -I$(SRC_DIR)
USER_LIB_DIRS	=

ifeq ($(HIGHBITDEPTH), 1)
HBD=HighBitDepth
else
HBD=
endif

# intermediate directory for object files
OBJ_DIR			= ./objects$(HBD)

# the library name
PRJ_NAME	 	= TAppCommon$(HBD)

# version information
MAJOR_VER		= 0
MINOR_VER		= 1
VER				= $(MAJOR_VER).$(MINOR_VER)

# defines to set
DEFS			= -DMSYS_LINUX

# set objects
OBJS          	= \
			$(OBJ_DIR)/program_options_lite.o \

LIBS				= -lpthread -I/usr/local/include -L/usr/local/lib -lopencv_viz -lopencv_superres -lopencv_objdetect -lopencv_stitching -lopencv_ml -lopencv_dnn -lopencv_videostab -lopencv_calib3d -lopencv_features2d -lopencv_flann -lopencv_highgui -lopencv_photo -lopencv_shape -lopencv_video -lopencv_videoio -lopencv_imgcodecs -lopencv_imgproc -lopencv_core

DEBUG_LIBS			=
RELEASE_LIBS		=

STAT_LIBS			=
DYN_LIBS			= -ldl

# the libraries to link with
STAT_DEBUG_LIBS		=
STAT_RELEASE_LIBS	=
DYN_DEBUG_LIBS		=
DYN_RELEASE_LIBS	=

# name of the base makefile
MAKE_FILE_NAME		= ../../common/makefile.base

# include the base makefile
include $(MAKE_FILE_NAME)
