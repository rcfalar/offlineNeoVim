# offlineNeoVim

Offline NeoVim package with **NvChad** pre-installed, including all plugins. This package is delivered as a **Base64 file** for easy copy/paste deployment on offline systems.

## Deployment Instructions

1. **Create the Base64 file on the target machine:**

```bash
cat > nvim-offline-full.b64
# (Paste the Base64 content here)
# Press Ctrl+D when done
```

2. **Decode and extract the archive:**

```bash
base64 -d nvim-offline-full.b64 > nvim-offline-full.tar.gz
tar xzf nvim-offline-full.tar.gz -C /home/rfalar
```

3. **Make the Neovim AppImage executable:**

```bash
chmod +x /home/rfalar/nvim.appimage
```

4. **Run Neovim:**

```bash
/home/rfalar/nvim.appimage
```

5. **Optional: Add `nvim` to your PATH for easy access**

```bash
echo 'export PATH=$HOME:$PATH' >> ~/.bashrc
source ~/.bashrc
```

* After this, you can just run `nvim` from any terminal.

---

### Included in this package

* **NvChad configuration**
* **All plugins pre-installed** (Telescope, Treesitter, etc.)
* **Mason LSP servers** installed and ready for offline use
* Fully self-contained **Neovim AppImage**
