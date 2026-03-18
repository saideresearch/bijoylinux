## Manual Configuration

The `bijoyLinux` repository has been updated recently (as of April 2025) with corrected Unicode mappings that should fix exactly this issue . Here's how to properly set it up:

### Step 1: Install Prerequisites

```bash
# Install required packages
sudo pacman -S ibus-m17n m17n-db m17n-lib
```

### Step 2: Get the Correct Configuration Files

```bash
# Clone the bijoyLinux repository
git clone https://github.com/nazdridoy/bijoyLinux.git
cd bijoyLinux
```

### Step 3: Install the Corrected Mapping Files

```bash
# Copy the Bijoy Unicode mapping to the m17n directory
sudo cp m17n.d/bn-bijoyUnicode.mim /usr/share/m17n/
sudo cp m17n.d/bn-bijoyClassic.mim /usr/share/m17n/
```

### Step 4: Configure IBus

1. Restart IBus:

```bash
ibus restart
```

2. Open IBus Preferences (from application menu or run `ibus-setup`)
3. Go to Input Method tab
4. Click Add → Find and add "Bengali - Bijoy Unicode" or "Bengali - Bijoy Classic"
5. Remove any other Bengali input methods
6. Set it as default

### Step 5: Test the Configuration

Open any text editor and try typing. The corrected mappings should now handle the vowel placement correctly.

Collected from: 

```
https://github.com/nazdridoy/bijoyLinux.git
```
