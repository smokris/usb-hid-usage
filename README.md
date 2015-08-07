# USB HID Usage → Text converter

C function for converting USB HID Usage values to text

## Example

    int main(void)
    {
        uint32_t usagePage = 0x02;
        uint32_t usage     = 0x04;
        printf("%04x:%04x  %s\n", usagePage, usage, getHidUsageText(usagePage, usage));
    }

Output:

    0002:0004  Spaceship Simulation Device
