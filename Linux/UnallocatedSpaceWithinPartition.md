# Unallocated Space within Partition

## Problem
You have a partition with let's say 500GB of space. 200GB of this space is used but only 20GB are available.
In gparted, this remaining space within the partition is greyed out and you get a warning "Unallocated space within partion."

## How to fix
This fix is only tested for the scenario where the unallocated space is at the end of the partition block.

Get the filesystem mount point (e.g. `/dev/sdb3`) and use the command `resize2fs /dev/sdb3`.
This will automatically resize the partition to use all it's available space.