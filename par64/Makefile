PROGRAM = par64

ESP_HK_DEMO = ../esp-homekit-demo

EXTRA_COMPONENTS = \
	extras/i2s_dma \
	extras/ws2812_i2s \
	extras/rboot-ota \
	extras/http-parser \
	$(abspath $(ESP_HK_DEMO)/components/wolfssl) \
	$(abspath $(ESP_HK_DEMO)/components/cJSON) \
	$(abspath $(ESP_HK_DEMO)/components/homekit)

FLASH_SIZE ?= 8
HOMEKIT_SPI_FLASH_BASE_ADDR ?= 0x7a000

EXTRA_CFLAGS += -I.. -DHOMEKIT_SHORT_APPLE_UUIDS

LIBS ?= hal m

include $(SDK_PATH)/common.mk

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 115200 --elf $(PROGRAM_OUT)
