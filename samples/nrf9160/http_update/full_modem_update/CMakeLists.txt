#
# Copyright (c) 2021 Nordic Semiconductor ASA
#
# SPDX-License-Identifier: LicenseRef-Nordic-5-Clause
#

cmake_minimum_required(VERSION 3.13.1)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(full_modem_update)

target_sources(app PRIVATE src/main.c)
target_sources(app PRIVATE ../common/src/update.c)
target_include_directories(app PRIVATE ../common/include)
