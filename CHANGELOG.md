# Changelog

## 2024-04-30

### Fixed
- Fixed build errors by removing unsupported configuration options:
  - Commented out `CONFIG_ZMK_LEADER_MAX_SEQUENCES_PER_KEY` and related options
  - Disabled display configuration options (`CONFIG_ZMK_DISPLAY_FULL_REFRESH_PERIOD`, etc.)
  - Disabled `CONFIG_PM` that was causing dependency errors

### Improved
- Enhanced Bluetooth connectivity between halves:
  - Increased Bluetooth transmit power from 0 dBm to +8 dBm
  - Added high-priority settings for Bluetooth central connections
  - Enabled 2M PHY mode for faster, more reliable Bluetooth
  - Increased receiver sensitivity with `CONFIG_BT_CTLR_RX_MINIMUM_POWER_PLUS_12`
  - Adjusted debounce values from 1ms to 5ms to reduce noise
- Modified power management settings:
  - Doubled idle timeout (15s → 30s)
  - Extended sleep timeout (5min → 10min)
  - Reduced battery report interval for better status updates