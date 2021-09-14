---
title: Format du fichier de thème
description: Ce document décrit le format des fichiers de thème (. Theme). un fichier. theme est un fichier texte .ini qui est divisé en sections, qui spécifient les éléments visuels qui apparaissent sur un bureau Windows. Les noms de section sont encapsulés entre crochets (\ \) dans le fichier .ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584e6d9785cf7660e017cadfb2a39d6bce6c2a87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115985"
---
# <a name="theme-file-format"></a>Format du fichier de thème

Ce document décrit le format des fichiers de thème (. Theme). un fichier. theme est un fichier texte .ini qui est divisé en sections, qui spécifient les éléments visuels qui apparaissent sur un bureau Windows. Les noms de section sont encapsulés entre crochets ( \[ \] ) dans le fichier .ini.

un nouveau format de fichier,. themepack, a été introduit avec Windows 7 pour aider les utilisateurs à partager des thèmes. les thèmes ne peuvent être sélectionnés dans le panneau de configuration de personnalisation que dans Windows 7 Édition Familiale Premium ou version ultérieure, ou uniquement sur Windows Server 2008 R2 lorsque le composant Desktop est installé.

Les rubriques suivantes sont présentées dans cet article.

-   [Création d’un fichier de thème](#creating-a-theme-file)
-   [Description d’un fichier de thème](#description-of-a-theme-file)
    -   [\[\]Section thème](#theme-section)
    -   [\[Section couleurs du panneau de configuration \\ \]](#control-panelcolors-section)
    -   [\[\\Section curseurs du panneau de configuration \]](#control-panelcursors-section)
    -   [\[Section Desktop du panneau de configuration \\ \]](#control-paneldesktop-section)
    -   [\[Section de diaporama \]](#slideshow-section)
    -   [\[Section mesures \]](#metrics-section)
    -   [\[Section styles visuels \]](#visual-styles-section)
    -   [\[\]Sections sons et \[ AppEvents \] (sons)](#sounds-and-appevents-sections-sounds)
    -   [\[Section de démarrage \]](#boot-section)
    -   [\[\]Section MasterThemeSelector](#masterthemeselector-section)
-   [Exemple de fichier de thème](#example-of-a-theme-file)
-   [Installation des fichiers de thème](#installing-theme-files)
-   [Packs de thèmes](#theme-packs)
-   [Rubriques connexes](#related-topics)

## <a name="creating-a-theme-file"></a>Création d’un fichier de thème

Un fichier. Theme vous permet de modifier l’apparence de certains éléments du bureau. Vous pouvez créer ou modifier un fichier. theme de deux façons :

-   Modifiez les paramètres de personnalisation ou d’affichage dans le panneau de configuration et enregistrez les paramètres sous la forme d’un fichier. Theme. pour obtenir des instructions, consultez l’aide de votre Windows.
-   Créez un fichier. Theme manuellement pour un niveau de contrôle supérieur sur les détails de votre thème.

Pour mettre votre thème à la disposition d’autres utilisateurs, vous devez fournir votre fichier. Theme, ainsi que l’image d’arrière-plan, l’économiseur d’écran et les fichiers d’icônes. Vous pouvez le faire avec un [Pack de thèmes](#theme-packs).

## <a name="description-of-a-theme-file"></a>Description d’un fichier de thème

Les fichiers de thème comportent un certain nombre de sections obligatoires et facultatives. Les sections suivantes décrivent les sections des fichiers. Theme et fournissent des exemples de spécification des modifications pour les différents éléments.

### <a name="theme-section"></a>\[\]Section thème

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres par défaut.

 

La \[ \] section thème identifie le nom de votre thème personnalisé et spécifie le logo de la personnalisation de votre thème et les icônes du bureau.

La première partie de la \[ \] section thème contient les deux éléments suivants :



| Élément                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName = nom<br/> ou<br/> DisplayName = @module ,-stringid<br/> exemple : DisplayName = @themeui.dll ,-2013 | DisplayName est le nom du thème qui s’affichera dans le panneau de configuration de personnalisation. Il peut s’agir d’une chaîne ou d’une référence à un nom localisé.<br/> Ce champ est facultatif. Si elle est manquante, le nom de fichier du thème est utilisé comme nom de thème.<br/>                                                                                                                                                                                                                                         |
| BrandImage = chemin d’accès à l’image<br/> exemple : BrandImage = c : \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 et versions ultérieures** BrandImage spécifie le chemin d’accès à un fichier graphique de personnalisation qui est incorporé dans l’aperçu du thème dans le panneau de configuration de personnalisation.<br/> L’icône graphique doit être un fichier PNG. Le graphique est mis à l’échelle en pixels 80x240. il est donc recommandé de fournir une image de cette taille. La Galerie de thèmes respecte les régions transparentes de votre icône de personnalisation.<br/> Ce champ est facultatif. S’il est manquant, aucun logo n’est affiché en tant qu’icône de thème.<br/> |



 

Le reste de la \[ \] section thème spécifie des icônes personnalisées pour les fonctionnalités de bureau telles que ordinateur, mes documents, réseau et corbeille. Si vous ne spécifiez pas d’icônes de bureau personnalisées, le bureau affiche les icônes du bureau par défaut du système.

Voici deux exemples de la manière dont un fichier. Theme définit l’icône de l' **ordinateur** .


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



les valeurs suivantes sont utilisées pour les icônes de bureau par défaut dans Windows 7.


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a>\[Section couleurs du panneau de configuration \\ \]

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres par défaut. Si votre thème utilise le style visuel Aero, vous devez éviter de remplacer les valeurs par défaut dans cette section.

 

La couleur des éléments, tels que les barres de défilement, le texte et les boutons, sont personnalisables. Le fichier. Theme spécifie les valeurs RVB à modifier pour ces éléments. les valeurs remplacent les valeurs par défaut du style visuel et sont utilisées lorsque votre thème est basé sur Windows thèmes classiques, Windows 7 de base ou contraste élevé.

Voici un exemple de la façon dont les couleurs sont définies.


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a>\[\\Section curseurs du panneau de configuration \]

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise des curseurs par défaut.

 

Un thème peut également modifier l’apparence des curseurs. pour ce faire, vous créez des fichiers. cur pour remplacer les curseurs par défaut Windows. L’exemple suivant provient d’un fichier. Theme qui définit les curseurs pour un thème appelé *Sports*.


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a>\[Section Desktop du panneau de configuration \\ \]

> [!Note]  
> Cette section est obligatoire. Si vous n’incluez pas cette section dans votre fichier. Theme, le système ignore votre thème et n’affiche pas le thème dans le panneau de configuration.

 

Vous pouvez créer un arrière-plan de bureau personnalisé et spécifier un chemin d’accès au fichier image. L’exemple suivant montre comment modifier l’apparence du bureau.


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a>\[Section de diaporama \]

**Windows 7 et versions ultérieures.**

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise l’image d’arrière-plan du Bureau spécifiée dans la \[ section Bureau du panneau de configuration \\ \] . Si vous incluez cette section, vous devez spécifier les paramètres du diaporama ici.

 

L’arrière-plan de votre thème peut être un diaporama d’images stockées localement ou d’images servies par un flux RSS. La \[ \] section de diaporama du fichier contient les attributs suivants :




| Attribut | Description | 
|-----------|-------------|
| Interval = nombre de millisecondes | Obligatoire. Interval est un nombre qui détermine la fréquence à laquelle l’arrière-plan est modifié. Il est mesuré en millisecondes. | 
| Lecture aléatoire = 0 ou 1 | Obligatoire. La lecture aléatoire identifie si l’arrière-plan est aléatoire.<br /> 0 - Désactivé<br /> 1 - Activé<br /> | 
| RSSFeed = URL du flux RSS | Obligatoire si ImagesRootPath n’est pas spécifié. RSSFeed spécifie un flux RSS à utiliser comme diaporama d’arrière-plan. pour que le flux fonctionne, vous devez référencer des images haute résolution qui adhèrent à la norme « boîtiers » utilisée par la <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">plateforme RSS Windows</a>. En raison de cette limitation, les fichiers. Theme qui incluent un flux RSS doivent être créés manuellement. <br /><blockquote>[!Note]<br />Vous ne pouvez pas spécifier à la fois un RSSFeed et un ImagesRootPath.</blockquote><br /><br /> | 
| ImagesRootPath = chemin d’accès au dossier image | Obligatoire si RSSFeed n’est pas spécifié. ImagesRootPath spécifie un chemin d’accès à un ensemble d’images que vous souhaitez utiliser comme arrière-plan de la diapositive d’arrière-plan. Les images des sous-dossiers ne sont pas incluses dans le diaporama.<br /> ImagesRootPath prend en charge les substitutions de variables d’environnement dans le chemin d’accès.<br /><blockquote>[!Note]<br />Vous ne pouvez pas spécifier à la fois un RSSFeed et un ImagesRootPath.</blockquote><br /><br /> | 
| Élément<em>N</em>Path = chemin (s) vers une ou plusieurs images spécifiques | Pour une utilisation avec ImagesRootPath. <br /> L’élément<em>N</em>Path spécifie les chemins d’accès à des images spécifiques, ce qui vous permet de limiter le diaporama à des images particulières au lieu de toutes les images d’un dossier. Si aucun chemin d’accès n’est spécifié, toutes les images du chemin d’accès ImagesRootPath sont utilisées dans le diaporama, y compris les images ajoutées après la création et l’installation du thème.<br /> L’élément<em>N</em>Path prend en charge les substitutions de variables d’environnement dans le chemin d’accès. <em>N</em> est 0, 1, 2, et ainsi de suite. <br /> | 




 

Les exemples suivants montrent comment un fichier. Theme spécifie le diaporama pour inclure un ensemble d’images stockées localement.


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



L’exemple suivant est un modèle pour un fichier. Theme qui crée un diaporama d’arrière-plan du Bureau à l’aide d’images à partir d’un flux RSS. Pour personnaliser le modèle, procédez comme suit :

1.  Copiez l’exemple suivant et collez-le dans un éditeur de texte.
2.  Remplacez {ThemeName} par le nom que vous souhaitez voir apparaître dans la Galerie de thèmes de personnalisation du panneau de configuration.
3.  Remplacez {rssfeedurl} par le chemin d’accès complet à un flux RSS compatible.
4.  Enregistrez les modifications dans un fichier avec l’extension « . Theme ».


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a>\[Section mesures \]

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres de style visuel par défaut.

 

Vous pouvez spécifier des mesures système dans un fichier. Theme. Les métriques du système sont les dimensions de divers éléments d’affichage, tels que la largeur de la bordure de la fenêtre, la hauteur de l’icône ou la largeur de barre de défilement. Les valeurs NonclientMetrics et IconMetrics sont des structures binaires définies par NONCLIENTMETRICS et ICONMETRICS dans winuser. h. Voici un exemple de modification des mesures système.


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a>\[Section styles visuels \]

> [!Note]  
> Cette section est obligatoire. Si vous n’incluez pas cette section dans votre fichier. Theme, le système ignore votre thème et n’affiche pas le thème dans le panneau de configuration.

 

Vous pouvez fournir des informations spécifiques concernant la taille et la couleur des éléments de bureau dans les fichiers. msstyles. Les sections de couleur et de taille des fichiers. Theme peuvent être remplacées par des fichiers. msstyles qui vous permettent de modifier les éléments du bureau plus en détail. Ces fichiers sont spécifiés dans la section des styles visuels d’un fichier. Theme. Voici un exemple de section de styles visuels.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



L’ajout d’un élément Path à un fichier. msstyles est facultatif. Si vous fournissez un chemin d’accès, vous devez supprimer les sections de mesures et de couleurs du fichier. Theme. Lorsque ces sections sont supprimées, les couleurs, les polices et les tailles d’un thème proviennent du fichier. msstyles et correspondent à l’intention de l’auteur. msstyles. l’impossibilité de supprimer les sections de métriques et de couleurs peut entraîner des problèmes de dessin de Windows ou d’applications.

**Windows Vista/Windows 7 :** Lorsque le chemin d’accès pointe vers Aero. msstyles, vous pouvez spécifier la couleur de transparence souhaitée, comme illustré dans l’exemple suivant.

**Windows 7 :** Lorsque le chemin d’accès pointe vers Aero. msstyles, vous pouvez également spécifier la valeur de transparence souhaitée, comme indiqué dans l’exemple suivant.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Si les valeurs de ColorizationColor et de transparence correspondent exactement à une couleur système, le panneau de configuration de personnalisation affiche le nom du système pour la couleur. Dans le cas contraire, la couleur est intitulée « Custom ».

l’exemple suivant montre une section VisualStyles pour le thème de base Windows 7.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



l’exemple suivant montre une section VisualStyles pour le thème Windows classique.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



L’exemple suivant montre une section VisualStyles pour un contraste élevé thème noir.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[\]Sections sons et \[ AppEvents \] (sons)

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres audio par défaut.

 

L’utilisateur peut sélectionner l’icône de **son** dans le panneau de configuration pour associer des sons à des événements qui se produisent dans les applications. Par exemple, un fichier. wav peut être lu lors de l’ouverture d’une application. Un fichier. Theme peut spécifier des fichiers. wav pour remplacer ceux par défaut. L’exemple suivant vous montre comment procéder.


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



**Windows 7 et versions ultérieures :** Vous pouvez spécifier un nom de modèle de son au lieu de répertorier chaque son séparément.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



La valeur SchemeName spécifie le nom du modèle de son ou le nom du modèle de son localisé, comme indiqué dans l’exemple ci-dessus.

### <a name="boot-section"></a>\[Section de démarrage \]

> [!Note]  
> **les économiseurs d’écran sont déconseillés dans la Windows 10 mise à jour anniversaire et au-delà.**

 

> [!Note]  
> Cette section est facultative. Si vous n’incluez pas cette section dans votre fichier. Theme, aucun écran de veille n’est utilisé.

 

dans le fichier. theme, vous pouvez spécifier l’économiseur d’écran pour Windows à utiliser. L'exemple suivant illustre cela.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[\]Section MasterThemeSelector

> [!Note]  
> Cette section est obligatoire. Si vous n’incluez pas cette section dans votre fichier. Theme, le système ignore votre thème et n’affiche pas le thème dans le panneau de configuration.

 

La section du sélecteur de thème maître du fichier. Theme doit toujours être incluse en tant que balise indiquant que le fichier est valide. Vous n’avez pas de choix de valeurs pour ce paramètre. Ce qui suit est décrit ci-dessous.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Exemple de fichier de thème

L’exemple suivant montre un fichier. Theme complet.


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a>Installation des fichiers de thème

lorsque Windows est initialisé, le système d’exploitation énumère les sous-répertoires de premier niveau des ressources% WinDir \\ % \\ pour identifier les thèmes disponibles. Les fichiers de thèmes du système par défaut se trouvent dans les thèmes% WinDir% \\ Resources \\ . les fichiers de thème utilisateur sont stockés dans% WinDir% \\ users \\ &lt; nom_utilisateur &gt; \\ AppData \\ Local \\ Microsoft \\ Windows \\ themes.

Un fichier. Theme a des associations de fichiers ; par conséquent, les applications de programme d’installation de thème peuvent appeler [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) sur un fichier. Theme pour ouvrir la fenêtre de **personnalisation** du panneau de configuration au thème spécifié.

## <a name="theme-packs"></a>Packs de thèmes

**Windows 7 et versions ultérieures.** Un pack de thèmes est un fichier de .cab qui contient non seulement le fichier. Theme, mais également les fichiers nécessaires pour implémenter le thème sur un autre ordinateur, tel que des fichiers audio et des images. Les utilisateurs peuvent créer des packs de thèmes par le biais du panneau de configuration de personnalisation.

Les types de fichiers pris en charge sont les suivants :



| Type de fichier    | Extension                           |
|--------------|-------------------------------------|
| Thème        | .theme                              |
| Image        | .jpg,. jpeg, .bmp,. dib,. TIF, .png |
| Son        | .wav                                |
| Curseur de la souris | . cur,. ani                          |
| Icône de bureau | .ico                                |
| Logo de la personnalisation   | .png                                |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des styles visuels](visual-styles-overview.md)
</dt> </dl>

