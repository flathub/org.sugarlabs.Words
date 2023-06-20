# Words Activity Flatpak

Words activity is a multilingual dictionary activity for the Sugar environment.

To know more refer https://github.com/sugarlabs/words-activity

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.Words.git
cd org.sugarlabs.Words
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.Words.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Words
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Words.json
```