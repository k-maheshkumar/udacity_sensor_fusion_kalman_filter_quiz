cmake_minimum_required (VERSION 3.0)
project (kalman_example)
 
find_package (Eigen3 3.3 REQUIRED NO_MODULE)
 
add_executable (kalman_1d src/kalman_1d/kalman.cpp)
target_link_libraries (kalman_1d Eigen3::Eigen)

add_executable (kalman_2d 
    src/kalman_2d/kalman_filter.cpp
    src/kalman_2d/tracking.cpp
    src/kalman_2d/main.cpp
)
target_link_libraries (kalman_2d Eigen3::Eigen)

add_executable (calc_rmse 
    src/kalman_2d/calc_rmse.cpp
)
target_link_libraries (calc_rmse Eigen3::Eigen)

add_executable (calc_jacobian 
    src/kalman_2d/calc_jacobian.cpp
)
target_link_libraries (calc_jacobian Eigen3::Eigen)

add_executable (ukf 
    src/ukf/ukf.cpp
    src/ukf/main.cpp
)
target_link_libraries (calc_rmse Eigen3::Eigen)