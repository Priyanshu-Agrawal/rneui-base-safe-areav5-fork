# Safe Area Context v5 Support

This fork of `@rneui/base` has been updated to support `react-native-safe-area-context` version 5.

## Changes Made

### 1. Updated Dependencies

**File: `packages/base/package.json`**

- **devDependencies**: Updated `react-native-safe-area-context` from `4.14.0` to `^5.0.0`
- **peerDependencies**: Updated `react-native-safe-area-context` from `>= 3.0.0` to `>= 5.0.0`

### 2. Code Compatibility Verification

The existing code is fully compatible with v5:

- ✅ `SafeAreaView` component - Still available and works the same way
- ✅ `Edge` type - Still exported from `react-native-safe-area-context`
- ✅ `edges` prop - Still supported on `SafeAreaView`

**Components using safe-area-context:**
- `Header` component (`packages/base/src/Header/Header.tsx`) - Uses `SafeAreaView` with `edges` prop
- `BottomSheet` component (`packages/base/src/BottomSheet/BottomSheet.tsx`) - Uses `SafeAreaView`

## Installation

To use this fork with `react-native-safe-area-context` v5:

```bash
# Install the fork (adjust path as needed)
npm install /path/to/rneui-base-fork/packages/base

# Install react-native-safe-area-context v5
npm install react-native-safe-area-context@^5.0.0

# For iOS, install pods
cd ios && pod install
```

## Requirements

- React Native >= 0.74 (required for safe-area-context v5)
- `react-native-safe-area-context` >= 5.0.0

## Notes

- The API remains backward compatible for the features used by `@rneui/base`
- No code changes were required - only dependency updates
- All existing functionality should work as before

