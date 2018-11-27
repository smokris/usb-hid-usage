# USB HID Usage → Text converter

C function for converting USB HID Usage values to text

## Example
```c
#include "usb-hid-usage.h"

#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    uint32_t usagePage = 0x02;
    uint32_t usage     = 0x04;
    char *usageText = getHidUsageText(usagePage, usage);
    printf("%04x:%04x  %s\n", usagePage, usage, usageText);
    free(usageText);
    return 0;
}
```

Output:

    0002:0004  Spaceship Simulation Device
