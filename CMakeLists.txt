# QPC Zephyr application template and example
# SPDX-License-Identifier: GPL-3.0-or-later OR LicenseRef-QL-commercial

cmake_minimum_required(VERSION 3.20.0)

set(ZEPHYR_EXTRA_MODULES ${CMAKE_CURRENT_SOURCE_DIR}/qpc-zephyr)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})

project(qpc-app)
target_sources(app PRIVATE
 src/main.c
 src/bsp.c
 src/philo.c
 src/table.c
)

