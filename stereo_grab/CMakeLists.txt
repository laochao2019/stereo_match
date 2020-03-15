# CMakeList.txt: stereo_match �� CMake ��Ŀ���ڴ˴�����Դ���벢����
# ��Ŀ�ض����߼���
#
cmake_minimum_required (VERSION 3.0.0)

# ��Դ�������ӵ�����Ŀ�Ŀ�ִ���ļ���
add_executable (stereo_grab "stereo_grab.cpp")
# TODO: ������Ҫ�������Ӳ��Բ���װĿ�ꡣ


# �ҵ�������������ͷ�����ð� 
set(HIKI_INCLUDE_DIR "${PROJECT_SOURCE_DIR}/include")
set(HIKI_LIB_DIR "${PROJECT_SOURCE_DIR}/lib/")
set(CAMERA_CONTROL_INCLUDE_DIR "${PROJECT_SOURCE_DIR}/hikivision_camera")
set(CAMERA_CONTROL_LIB_DIR "${PROJECT_SOURCE_DIR}/include")
message("HIKI_INCLUDE_DIR: ${HIKI_INCLUDE_DIR}")
message("HIKI_LIB_DIR: ${HIKI_LIB_DIR}")
include_directories(${HIKI_INCLUDE_DIR})
link_directories(${HIKI_LIB_DIR})



# ����OpenCV���ļ�
target_link_libraries(stereo_grab ${OpenCV_LIBS})