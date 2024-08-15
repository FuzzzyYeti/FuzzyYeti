---
title: Study GameHacking
description: Study Basic of Cheat Engine
author: FuzzyYeti
date: 2024-08-12 21:21 +0800
categories: [GameHacking]
---

## Modifying Memory Using Cheat Engine

Cheat Engine primarily utilizes the Windows API function `WriteProcessMemory` to modify the memory of other processes. This function is used to write data to a specific memory address within a process.

### `WriteProcessMemory` Function

#### Function Prototype

```c
BOOL WriteProcessMemory(
  [in]  HANDLE  hProcess,               // Handle to the target process
  [in]  LPVOID  lpBaseAddress,          // Memory address to start writing
  [in]  LPCVOID lpBuffer,               // Buffer containing the data to write
  [in]  SIZE_T  nSize,                  // Size of the data to write, in bytes
  [out] SIZE_T  *lpNumberOfBytesWritten // Number of bytes actually written
);
```


## Basic Functions

### Opening a Process

1. **Start Cheat Engine**.
2. **Click the Computer Icon**:
   - Located in the top-left corner of Cheat Engine's main window. This opens a list of currently running processes.
3. **Select the Target Process**:
   - Choose the process you want to modify (e.g., a game) and click "Open."


### Scanning for Values

1. **Enter the Value**:
   - Type the value you want to search for in the "Value" field.
2. **Choose the Value Type**:
   - Select the data type (e.g., 4 Bytes, Float) that matches the value you are searching for.
3. **Click "First Scan"**:
   - Cheat Engine will search for the specified value in the selected process's memory.   


### Modifying Values

1. **Find the Value**:
   - After the scan, a list of addresses will appear. Change the value in the game or application and perform a new scan to narrow down the results.
2. **Double-Click to Add to List**:
   - Select the address you want to modify and double-click to add it to the address list.
3. **Change the Value**:
   - In the address list, double-click on the value field and enter the new value you want.

### Example 1: Gold Value Modification

**Before Modification**:

![Before Modification](/assets/GameHacking-Study/CheatEngine-01-before.png){: .normal}

**After Modification**:

![Desktop View](/assets/GameHacking-Study/CheatEngine-01-result.png){: .normal }

*Description: Modified the gold value in the game to increase health from 200 to 9999999.*

