# Using the Fork with @rneui/themed

## Installation

To use this fork with `@rneui/themed` and ensure compatibility:

### Option 1: Install both from your fork (Recommended)

**Important:** Install from the `packages/base` subdirectory:

```bash
npm install \
  https://github.com/Priyanshu-Agrawal/rneui-base-safe-areav5-fork.git#main:packages/base \
  @rneui/themed
```

Or using the shorthand (after the fix):
```bash
npm install \
  https://github.com/Priyanshu-Agrawal/rneui-base-safe-areav5-fork.git#main \
  @rneui/themed
```

### Option 2: Use npm/yarn resolutions (if using original @rneui/themed)

Add to your `package.json`:

```json
{
  "resolutions": {
    "@rneui/base": "https://github.com/Priyanshu-Agrawal/rneui-base-safe-areav5-fork.git#main"
  }
}
```

Or for npm (using `overrides`):

```json
{
  "overrides": {
    "@rneui/base": "https://github.com/Priyanshu-Agrawal/rneui-base-safe-areav5-fork.git#main"
  }
}
```

### Option 3: Direct installation

```bash
npm install @rneui/themed
npm install https://github.com/Priyanshu-Agrawal/rneui-base-safe-areav5-fork.git#main
```

**Note:** The postinstall script has been fixed to not cause errors when installing as a dependency. If you still encounter issues, try:
```bash
npm install --ignore-scripts https://github.com/Priyanshu-Agrawal/rneui-base-safe-areav5-fork.git#main
```

## Compatibility

✅ **Works with:**
- `@rneui/themed` (original from npm) - because version `4.0.0-rc.8` matches
- All other RNEUI packages that depend on `@rneui/base`
- `react-native-safe-area-context` v5

⚠️ **Important:**
- Make sure `react-native-safe-area-context@^5.0.0` is installed in your project
- The original `@rneui/base` from npm requires `react-native-safe-area-context >= 3.0.0`, but your fork requires `>= 5.0.0`

## Example Usage

```javascript
import { ThemeProvider } from '@rneui/themed';
import { Header } from '@rneui/themed';
// Your fork of @rneui/base will be used automatically
```

