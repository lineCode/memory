# Copyright (C) 2015-2020 Jonathan Müller <jonathanmueller.dev@gmail.com>
# This file is subject to the license terms in the LICENSE file
# found in the top-level directory of this distribution.

# builds examples

macro(_foonathan_add_example name)
    add_executable(foonathan_memory_example_${name} ${name}.cpp)
    target_link_libraries(foonathan_memory_example_${name} PRIVATE foonathan_memory)
endmacro()

_foonathan_add_example(allocator_storage)
_foonathan_add_example(joint_allocation)
_foonathan_add_example(taking_allocators)
_foonathan_add_example(tracking)
_foonathan_add_example(using_allocators)
