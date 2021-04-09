---
title: Format du fichier de thème
description: Ce document décrit le format des fichiers de thème (. Theme). Un fichier. Theme est un fichier texte. ini divisé en sections, qui spécifient les éléments visuels qui apparaissent sur un bureau Windows. Les noms de section sont encapsulés entre crochets (\ \) dans le fichier. ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "103842853"
---
# <a name="theme-file-format"></a><span data-ttu-id="5dabe-105">Format du fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-105">Theme File Format</span></span>

<span data-ttu-id="5dabe-106">Ce document décrit le format des fichiers de thème (. Theme).</span><span class="sxs-lookup"><span data-stu-id="5dabe-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="5dabe-107">Un fichier. Theme est un fichier texte. ini divisé en sections, qui spécifient les éléments visuels qui apparaissent sur un bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="5dabe-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="5dabe-108">Les noms de section sont encapsulés entre crochets ( \[ \] ) dans le fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="5dabe-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="5dabe-109">Un nouveau format de fichier,. themepack, a été introduit avec Windows 7 pour aider les utilisateurs à partager des thèmes.</span><span class="sxs-lookup"><span data-stu-id="5dabe-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="5dabe-110">Les thèmes peuvent être sélectionnés dans le panneau de configuration personnalisation uniquement dans Windows 7 Édition familiale Premium ou version ultérieure, ou uniquement sur Windows Server 2008 R2 lorsque le composant Desktop est installé.</span><span class="sxs-lookup"><span data-stu-id="5dabe-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="5dabe-111">Les rubriques suivantes sont présentées dans cet article.</span><span class="sxs-lookup"><span data-stu-id="5dabe-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="5dabe-112">Création d’un fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="5dabe-113">Description d’un fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="5dabe-114">[\[\]Section thème](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="5dabe-115">[\[Section couleurs du panneau de configuration \\ \]](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="5dabe-116">[\[\\Section curseurs du panneau de configuration \]](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="5dabe-117">[\[Section Desktop du panneau de configuration \\ \]](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="5dabe-118">[\[Section de diaporama \]](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="5dabe-119">[\[Section mesures \]](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="5dabe-120">[\[Section styles visuels \]](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="5dabe-121">[\[\]Sections sons et \[ AppEvents \] (sons)](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="5dabe-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="5dabe-122">[\[Section de démarrage \]](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="5dabe-123">[\[\]Section MasterThemeSelector](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="5dabe-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="5dabe-124">Exemple de fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="5dabe-125">Installation des fichiers de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="5dabe-126">Packs de thèmes</span><span class="sxs-lookup"><span data-stu-id="5dabe-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="5dabe-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5dabe-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="5dabe-128">Création d’un fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-128">Creating a Theme File</span></span>

<span data-ttu-id="5dabe-129">Un fichier. Theme vous permet de modifier l’apparence de certains éléments du bureau.</span><span class="sxs-lookup"><span data-stu-id="5dabe-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="5dabe-130">Vous pouvez créer ou modifier un fichier. theme de deux façons :</span><span class="sxs-lookup"><span data-stu-id="5dabe-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="5dabe-131">Modifiez les paramètres de personnalisation ou d’affichage dans le panneau de configuration et enregistrez les paramètres sous la forme d’un fichier. Theme.</span><span class="sxs-lookup"><span data-stu-id="5dabe-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="5dabe-132">Pour obtenir des instructions, consultez l’aide de Windows.</span><span class="sxs-lookup"><span data-stu-id="5dabe-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="5dabe-133">Créez un fichier. Theme manuellement pour un niveau de contrôle supérieur sur les détails de votre thème.</span><span class="sxs-lookup"><span data-stu-id="5dabe-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="5dabe-134">Pour mettre votre thème à la disposition d’autres utilisateurs, vous devez fournir votre fichier. Theme, ainsi que l’image d’arrière-plan, l’économiseur d’écran et les fichiers d’icônes.</span><span class="sxs-lookup"><span data-stu-id="5dabe-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="5dabe-135">Vous pouvez le faire avec un [Pack de thèmes](#theme-packs).</span><span class="sxs-lookup"><span data-stu-id="5dabe-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="5dabe-136">Description d’un fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-136">Description of a Theme File</span></span>

<span data-ttu-id="5dabe-137">Les fichiers de thème comportent un certain nombre de sections obligatoires et facultatives.</span><span class="sxs-lookup"><span data-stu-id="5dabe-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="5dabe-138">Les sections suivantes décrivent les sections des fichiers. Theme et fournissent des exemples de spécification des modifications pour les différents éléments.</span><span class="sxs-lookup"><span data-stu-id="5dabe-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="5dabe-139">\[\]Section thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-140">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-140">This section is optional.</span></span> <span data-ttu-id="5dabe-141">Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="5dabe-142">La \[ \] section thème identifie le nom de votre thème personnalisé et spécifie le logo de la personnalisation de votre thème et les icônes du bureau.</span><span class="sxs-lookup"><span data-stu-id="5dabe-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="5dabe-143">La première partie de la \[ \] section thème contient les deux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5dabe-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="5dabe-144">Élément</span><span class="sxs-lookup"><span data-stu-id="5dabe-144">Element</span></span>                                                                                                                    | <span data-ttu-id="5dabe-145">Description</span><span class="sxs-lookup"><span data-stu-id="5dabe-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dabe-146">DisplayName = nom</span><span class="sxs-lookup"><span data-stu-id="5dabe-146">DisplayName=name</span></span><br/> <span data-ttu-id="5dabe-147">ou</span><span class="sxs-lookup"><span data-stu-id="5dabe-147">or</span></span><br/> <span data-ttu-id="5dabe-148">DisplayName = @module ,-stringid</span><span class="sxs-lookup"><span data-stu-id="5dabe-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="5dabe-149">exemple : DisplayName = @themeui.dll ,-2013</span><span class="sxs-lookup"><span data-stu-id="5dabe-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="5dabe-150">DisplayName est le nom du thème qui s’affichera dans le panneau de configuration de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="5dabe-151">Il peut s’agir d’une chaîne ou d’une référence à un nom localisé.</span><span class="sxs-lookup"><span data-stu-id="5dabe-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="5dabe-152">Ce champ est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5dabe-152">This field is optional.</span></span> <span data-ttu-id="5dabe-153">Si elle est manquante, le nom de fichier du thème est utilisé comme nom de thème.</span><span class="sxs-lookup"><span data-stu-id="5dabe-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="5dabe-154">BrandImage = chemin d’accès à l’image</span><span class="sxs-lookup"><span data-stu-id="5dabe-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="5dabe-155">exemple : BrandImage = c : \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="5dabe-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="5dabe-156">**Windows 7 et versions ultérieures** BrandImage spécifie le chemin d’accès à un fichier graphique de personnalisation qui est incorporé dans l’aperçu du thème dans le panneau de configuration de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="5dabe-157">L’icône graphique doit être un fichier PNG.</span><span class="sxs-lookup"><span data-stu-id="5dabe-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="5dabe-158">Le graphique est mis à l’échelle en pixels 80x240. il est donc recommandé de fournir une image de cette taille.</span><span class="sxs-lookup"><span data-stu-id="5dabe-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="5dabe-159">La Galerie de thèmes respecte les régions transparentes de votre icône de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="5dabe-160">Ce champ est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5dabe-160">This field is optional.</span></span> <span data-ttu-id="5dabe-161">S’il est manquant, aucun logo n’est affiché en tant qu’icône de thème.</span><span class="sxs-lookup"><span data-stu-id="5dabe-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="5dabe-162">Le reste de la \[ \] section thème spécifie des icônes personnalisées pour les fonctionnalités de bureau telles que ordinateur, mes documents, réseau et corbeille.</span><span class="sxs-lookup"><span data-stu-id="5dabe-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="5dabe-163">Si vous ne spécifiez pas d’icônes de bureau personnalisées, le bureau affiche les icônes du bureau par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="5dabe-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="5dabe-164">Voici deux exemples de la manière dont un fichier. Theme définit l’icône de l' **ordinateur** .</span><span class="sxs-lookup"><span data-stu-id="5dabe-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="5dabe-165">Les valeurs suivantes sont utilisées pour les icônes de bureau par défaut dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5dabe-165">The following are values for the default desktop icons in Windows 7.</span></span>


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



### <a name="control-panelcolors-section"></a><span data-ttu-id="5dabe-166">\[Section couleurs du panneau de configuration \\ \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-167">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-167">This section is optional.</span></span> <span data-ttu-id="5dabe-168">Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="5dabe-169">Si votre thème utilise le style visuel Aero, vous devez éviter de remplacer les valeurs par défaut dans cette section.</span><span class="sxs-lookup"><span data-stu-id="5dabe-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="5dabe-170">La couleur des éléments, tels que les barres de défilement, le texte et les boutons, sont personnalisables.</span><span class="sxs-lookup"><span data-stu-id="5dabe-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="5dabe-171">Le fichier. Theme spécifie les valeurs RVB à modifier pour ces éléments.</span><span class="sxs-lookup"><span data-stu-id="5dabe-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="5dabe-172">Les valeurs remplacent les valeurs par défaut du style visuel et sont utilisées lorsque votre thème est basé sur les thèmes Windows Classic, Windows 7 de base ou contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="5dabe-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="5dabe-173">Voici un exemple de la façon dont les couleurs sont définies.</span><span class="sxs-lookup"><span data-stu-id="5dabe-173">Following is an example of how colors are set.</span></span>


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



### <a name="control-panelcursors-section"></a><span data-ttu-id="5dabe-174">\[\\Section curseurs du panneau de configuration \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-175">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-175">This section is optional.</span></span> <span data-ttu-id="5dabe-176">Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise des curseurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="5dabe-177">Un thème peut également modifier l’apparence des curseurs.</span><span class="sxs-lookup"><span data-stu-id="5dabe-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="5dabe-178">Pour ce faire, vous créez des fichiers. cur pour remplacer les curseurs Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="5dabe-179">L’exemple suivant provient d’un fichier. Theme qui définit les curseurs pour un thème appelé *Sports*.</span><span class="sxs-lookup"><span data-stu-id="5dabe-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


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



### <a name="control-paneldesktop-section"></a><span data-ttu-id="5dabe-180">\[Section Desktop du panneau de configuration \\ \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-181">Cette section est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5dabe-181">This section is required.</span></span> <span data-ttu-id="5dabe-182">Si vous n’incluez pas cette section dans votre fichier. Theme, le système ignore votre thème et n’affiche pas le thème dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5dabe-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="5dabe-183">Vous pouvez créer un arrière-plan de bureau personnalisé et spécifier un chemin d’accès au fichier image.</span><span class="sxs-lookup"><span data-stu-id="5dabe-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="5dabe-184">L’exemple suivant montre comment modifier l’apparence du bureau.</span><span class="sxs-lookup"><span data-stu-id="5dabe-184">The following example shows how to modify the desktop appearance.</span></span>


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



### <a name="slideshow-section"></a><span data-ttu-id="5dabe-185">\[Section de diaporama \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="5dabe-186">**Windows 7 et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="5dabe-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-187">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-187">This section is optional.</span></span> <span data-ttu-id="5dabe-188">Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise l’image d’arrière-plan du Bureau spécifiée dans la \[ section Bureau du panneau de configuration \\ \] .</span><span class="sxs-lookup"><span data-stu-id="5dabe-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="5dabe-189">Si vous incluez cette section, vous devez spécifier les paramètres du diaporama ici.</span><span class="sxs-lookup"><span data-stu-id="5dabe-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="5dabe-190">L’arrière-plan de votre thème peut être un diaporama d’images stockées localement ou d’images servies par un flux RSS.</span><span class="sxs-lookup"><span data-stu-id="5dabe-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="5dabe-191">La \[ \] section de diaporama du fichier contient les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="5dabe-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5dabe-192">Attribut</span><span class="sxs-lookup"><span data-stu-id="5dabe-192">Attribute</span></span></th>
<th><span data-ttu-id="5dabe-193">Description</span><span class="sxs-lookup"><span data-stu-id="5dabe-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5dabe-194">Interval = nombre de millisecondes</span><span class="sxs-lookup"><span data-stu-id="5dabe-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="5dabe-195">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5dabe-195">Required.</span></span> <span data-ttu-id="5dabe-196">Interval est un nombre qui détermine la fréquence à laquelle l’arrière-plan est modifié.</span><span class="sxs-lookup"><span data-stu-id="5dabe-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="5dabe-197">Il est mesuré en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="5dabe-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5dabe-198">Lecture aléatoire = 0 ou 1</span><span class="sxs-lookup"><span data-stu-id="5dabe-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="5dabe-199">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5dabe-199">Required.</span></span> <span data-ttu-id="5dabe-200">La lecture aléatoire identifie si l’arrière-plan est aléatoire.</span><span class="sxs-lookup"><span data-stu-id="5dabe-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="5dabe-201">0 - Désactivé</span><span class="sxs-lookup"><span data-stu-id="5dabe-201">0 = Disabled</span></span><br/> <span data-ttu-id="5dabe-202">1 - Activé</span><span class="sxs-lookup"><span data-stu-id="5dabe-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5dabe-203">RSSFeed = URL du flux RSS</span><span class="sxs-lookup"><span data-stu-id="5dabe-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="5dabe-204">Obligatoire si ImagesRootPath n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="5dabe-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="5dabe-205">RSSFeed spécifie un flux RSS à utiliser comme diaporama d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5dabe-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="5dabe-206">Pour que le flux fonctionne, vous devez référencer des images haute résolution qui adhèrent aux &quot; boîtiers &quot; standard utilisés par la <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">plateforme Windows RSS</a>.</span><span class="sxs-lookup"><span data-stu-id="5dabe-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="5dabe-207">En raison de cette limitation, les fichiers. Theme qui incluent un flux RSS doivent être créés manuellement.</span><span class="sxs-lookup"><span data-stu-id="5dabe-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5dabe-208">Vous ne pouvez pas spécifier à la fois un RSSFeed et un ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="5dabe-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5dabe-209">ImagesRootPath = chemin d’accès au dossier image</span><span class="sxs-lookup"><span data-stu-id="5dabe-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="5dabe-210">Obligatoire si RSSFeed n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="5dabe-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="5dabe-211">ImagesRootPath spécifie un chemin d’accès à un ensemble d’images que vous souhaitez utiliser comme arrière-plan de la diapositive d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="5dabe-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="5dabe-212">Les images des sous-dossiers ne sont pas incluses dans le diaporama.</span><span class="sxs-lookup"><span data-stu-id="5dabe-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="5dabe-213">ImagesRootPath prend en charge les substitutions de variables d’environnement dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="5dabe-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="5dabe-214">Vous ne pouvez pas spécifier à la fois un RSSFeed et un ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="5dabe-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5dabe-215">Élément<em>N</em>Path = chemin (s) vers une ou plusieurs images spécifiques</span><span class="sxs-lookup"><span data-stu-id="5dabe-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="5dabe-216">Pour une utilisation avec ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="5dabe-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="5dabe-217">L’élément<em>N</em>Path spécifie les chemins d’accès à des images spécifiques, ce qui vous permet de limiter le diaporama à des images particulières au lieu de toutes les images d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="5dabe-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="5dabe-218">Si aucun chemin d’accès n’est spécifié, toutes les images du chemin d’accès ImagesRootPath sont utilisées dans le diaporama, y compris les images ajoutées après la création et l’installation du thème.</span><span class="sxs-lookup"><span data-stu-id="5dabe-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="5dabe-219">L’élément<em>N</em>Path prend en charge les substitutions de variables d’environnement dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="5dabe-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="5dabe-220"><em>N</em> est 0, 1, 2, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="5dabe-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5dabe-221">Les exemples suivants montrent comment un fichier. Theme spécifie le diaporama pour inclure un ensemble d’images stockées localement.</span><span class="sxs-lookup"><span data-stu-id="5dabe-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


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



<span data-ttu-id="5dabe-222">L’exemple suivant est un modèle pour un fichier. Theme qui crée un diaporama d’arrière-plan du Bureau à l’aide d’images à partir d’un flux RSS.</span><span class="sxs-lookup"><span data-stu-id="5dabe-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="5dabe-223">Pour personnaliser le modèle, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5dabe-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="5dabe-224">Copiez l’exemple suivant et collez-le dans un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="5dabe-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="5dabe-225">Remplacez {ThemeName} par le nom que vous souhaitez voir apparaître dans la Galerie de thèmes de personnalisation du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5dabe-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="5dabe-226">Remplacez {rssfeedurl} par le chemin d’accès complet à un flux RSS compatible.</span><span class="sxs-lookup"><span data-stu-id="5dabe-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="5dabe-227">Enregistrez les modifications dans un fichier avec l’extension « . Theme ».</span><span class="sxs-lookup"><span data-stu-id="5dabe-227">Save the changes as a file with the ".theme" extension.</span></span>


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



### <a name="metrics-section"></a><span data-ttu-id="5dabe-228">\[Section mesures \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-229">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-229">This section is optional.</span></span> <span data-ttu-id="5dabe-230">Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres de style visuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="5dabe-231">Vous pouvez spécifier des mesures système dans un fichier. Theme.</span><span class="sxs-lookup"><span data-stu-id="5dabe-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="5dabe-232">Les métriques du système sont les dimensions de divers éléments d’affichage, tels que la largeur de la bordure de la fenêtre, la hauteur de l’icône ou la largeur de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="5dabe-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="5dabe-233">Les valeurs NonclientMetrics et IconMetrics sont des structures binaires définies par NONCLIENTMETRICS et ICONMETRICS dans winuser. h.</span><span class="sxs-lookup"><span data-stu-id="5dabe-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="5dabe-234">Voici un exemple de modification des mesures système.</span><span class="sxs-lookup"><span data-stu-id="5dabe-234">Following is an example of how to change system metrics.</span></span>


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



### <a name="visual-styles-section"></a><span data-ttu-id="5dabe-235">\[Section styles visuels \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-236">Cette section est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5dabe-236">This section is required.</span></span> <span data-ttu-id="5dabe-237">Si vous n’incluez pas cette section dans votre fichier. Theme, le système ignore votre thème et n’affiche pas le thème dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5dabe-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="5dabe-238">Vous pouvez fournir des informations spécifiques concernant la taille et la couleur des éléments de bureau dans les fichiers. msstyles.</span><span class="sxs-lookup"><span data-stu-id="5dabe-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="5dabe-239">Les sections de couleur et de taille des fichiers. Theme peuvent être remplacées par des fichiers. msstyles qui vous permettent de modifier les éléments du bureau plus en détail.</span><span class="sxs-lookup"><span data-stu-id="5dabe-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="5dabe-240">Ces fichiers sont spécifiés dans la section des styles visuels d’un fichier. Theme.</span><span class="sxs-lookup"><span data-stu-id="5dabe-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="5dabe-241">Voici un exemple de section de styles visuels.</span><span class="sxs-lookup"><span data-stu-id="5dabe-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="5dabe-242">L’ajout d’un élément Path à un fichier. msstyles est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5dabe-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="5dabe-243">Si vous fournissez un chemin d’accès, vous devez supprimer les sections de mesures et de couleurs du fichier. Theme.</span><span class="sxs-lookup"><span data-stu-id="5dabe-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="5dabe-244">Lorsque ces sections sont supprimées, les couleurs, les polices et les tailles d’un thème proviennent du fichier. msstyles et correspondent à l’intention de l’auteur. msstyles.</span><span class="sxs-lookup"><span data-stu-id="5dabe-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="5dabe-245">L’impossibilité de supprimer les sections de métriques et de couleurs peut entraîner des problèmes de dessin dans les fenêtres ou les applications.</span><span class="sxs-lookup"><span data-stu-id="5dabe-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="5dabe-246">**Windows Vista/Windows 7 :** Lorsque le chemin d’accès pointe vers Aero. msstyles, vous pouvez spécifier la couleur de transparence souhaitée, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5dabe-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="5dabe-247">**Windows 7 :** Lorsque le chemin d’accès pointe vers Aero. msstyles, vous pouvez également spécifier la valeur de transparence souhaitée, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5dabe-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="5dabe-248">Si les valeurs de ColorizationColor et de transparence correspondent exactement à une couleur système, le panneau de configuration de personnalisation affiche le nom du système pour la couleur.</span><span class="sxs-lookup"><span data-stu-id="5dabe-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="5dabe-249">Dans le cas contraire, la couleur est intitulée « Custom ».</span><span class="sxs-lookup"><span data-stu-id="5dabe-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="5dabe-250">L’exemple suivant montre une section VisualStyles pour le thème de base Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5dabe-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="5dabe-251">L’exemple suivant montre une section VisualStyles pour le thème Windows classique.</span><span class="sxs-lookup"><span data-stu-id="5dabe-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="5dabe-252">L’exemple suivant montre une section VisualStyles pour un contraste élevé thème noir.</span><span class="sxs-lookup"><span data-stu-id="5dabe-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="5dabe-253">\[\]Sections sons et \[ AppEvents \] (sons)</span><span class="sxs-lookup"><span data-stu-id="5dabe-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-254">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-254">This section is optional.</span></span> <span data-ttu-id="5dabe-255">Si vous n’incluez pas cette section dans votre fichier. Theme, le système utilise les paramètres audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="5dabe-256">L’utilisateur peut sélectionner l’icône de **son** dans le panneau de configuration pour associer des sons à des événements qui se produisent dans les applications.</span><span class="sxs-lookup"><span data-stu-id="5dabe-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="5dabe-257">Par exemple, un fichier. wav peut être lu lors de l’ouverture d’une application.</span><span class="sxs-lookup"><span data-stu-id="5dabe-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="5dabe-258">Un fichier. Theme peut spécifier des fichiers. wav pour remplacer ceux par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dabe-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="5dabe-259">L’exemple suivant vous montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="5dabe-259">The following example shows how to do this.</span></span>


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



<span data-ttu-id="5dabe-260">**Windows 7 et versions ultérieures :** Vous pouvez spécifier un nom de modèle de son au lieu de répertorier chaque son séparément.</span><span class="sxs-lookup"><span data-stu-id="5dabe-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="5dabe-261">La valeur SchemeName spécifie le nom du modèle de son ou le nom du modèle de son localisé, comme indiqué dans l’exemple ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5dabe-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="5dabe-262">\[Section de démarrage \]</span><span class="sxs-lookup"><span data-stu-id="5dabe-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-263">**Les économiseurs d’écran sont déconseillés dans la mise à jour anniversaire Windows 10 et au-delà.**</span><span class="sxs-lookup"><span data-stu-id="5dabe-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="5dabe-264">Cette section est facultative.</span><span class="sxs-lookup"><span data-stu-id="5dabe-264">This section is optional.</span></span> <span data-ttu-id="5dabe-265">Si vous n’incluez pas cette section dans votre fichier. Theme, aucun écran de veille n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5dabe-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="5dabe-266">Dans le fichier. Theme, vous pouvez spécifier l’économiseur d’écran pour Windows à utiliser.</span><span class="sxs-lookup"><span data-stu-id="5dabe-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="5dabe-267">L'exemple suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="5dabe-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="5dabe-268">\[\]Section MasterThemeSelector</span><span class="sxs-lookup"><span data-stu-id="5dabe-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="5dabe-269">Cette section est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5dabe-269">This section is required.</span></span> <span data-ttu-id="5dabe-270">Si vous n’incluez pas cette section dans votre fichier. Theme, le système ignore votre thème et n’affiche pas le thème dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5dabe-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="5dabe-271">La section du sélecteur de thème maître du fichier. Theme doit toujours être incluse en tant que balise indiquant que le fichier est valide.</span><span class="sxs-lookup"><span data-stu-id="5dabe-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="5dabe-272">Vous n’avez pas de choix de valeurs pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="5dabe-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="5dabe-273">Ce qui suit est décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5dabe-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="5dabe-274">Exemple de fichier de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-274">Example of a Theme File</span></span>

<span data-ttu-id="5dabe-275">L’exemple suivant montre un fichier. Theme complet.</span><span class="sxs-lookup"><span data-stu-id="5dabe-275">The following example shows a complete .theme file.</span></span>


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



## <a name="installing-theme-files"></a><span data-ttu-id="5dabe-276">Installation des fichiers de thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-276">Installing Theme Files</span></span>

<span data-ttu-id="5dabe-277">Lorsque Windows est initialisé, le système d’exploitation énumère les sous-répertoires de premier niveau des ressources% WinDir \\ % \\ pour identifier les thèmes disponibles.</span><span class="sxs-lookup"><span data-stu-id="5dabe-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="5dabe-278">Les fichiers de thèmes du système par défaut se trouvent dans les thèmes% WinDir% \\ Resources \\ .</span><span class="sxs-lookup"><span data-stu-id="5dabe-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="5dabe-279">Les fichiers de thème utilisateur sont stockés dans% windir% \\ Users \\ <username> \\ AppData \\ local \\ Microsoft \\ Windows \\ Themes.</span><span class="sxs-lookup"><span data-stu-id="5dabe-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="5dabe-280">Un fichier. Theme a des associations de fichiers ; par conséquent, les applications de programme d’installation de thème peuvent appeler [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) sur un fichier. Theme pour ouvrir la fenêtre de **personnalisation** du panneau de configuration au thème spécifié.</span><span class="sxs-lookup"><span data-stu-id="5dabe-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="5dabe-281">Packs de thèmes</span><span class="sxs-lookup"><span data-stu-id="5dabe-281">Theme Packs</span></span>

<span data-ttu-id="5dabe-282">**Windows 7 et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="5dabe-282">**Windows 7 and later.**</span></span> <span data-ttu-id="5dabe-283">Un pack de thèmes est un fichier. cab qui contient non seulement le fichier. Theme, mais également les fichiers nécessaires pour implémenter le thème sur un autre ordinateur, tel que des fichiers audio et des images.</span><span class="sxs-lookup"><span data-stu-id="5dabe-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="5dabe-284">Les utilisateurs peuvent créer des packs de thèmes par le biais du panneau de configuration de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="5dabe-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="5dabe-285">Les types de fichiers pris en charge sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5dabe-285">Supported file types include the following:</span></span>



| <span data-ttu-id="5dabe-286">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="5dabe-286">File type</span></span>    | <span data-ttu-id="5dabe-287">Extension</span><span class="sxs-lookup"><span data-stu-id="5dabe-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="5dabe-288">Thème</span><span class="sxs-lookup"><span data-stu-id="5dabe-288">Theme</span></span>        | <span data-ttu-id="5dabe-289">.theme</span><span class="sxs-lookup"><span data-stu-id="5dabe-289">.theme</span></span>                              |
| <span data-ttu-id="5dabe-290">Image</span><span class="sxs-lookup"><span data-stu-id="5dabe-290">Image</span></span>        | <span data-ttu-id="5dabe-291">. jpg,. jpeg,. bmp,. dib,. TIF,. png</span><span class="sxs-lookup"><span data-stu-id="5dabe-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="5dabe-292">Son</span><span class="sxs-lookup"><span data-stu-id="5dabe-292">Sound</span></span>        | <span data-ttu-id="5dabe-293">.wav</span><span class="sxs-lookup"><span data-stu-id="5dabe-293">.wav</span></span>                                |
| <span data-ttu-id="5dabe-294">Curseur de la souris</span><span class="sxs-lookup"><span data-stu-id="5dabe-294">Mouse cursor</span></span> | <span data-ttu-id="5dabe-295">. cur,. ani</span><span class="sxs-lookup"><span data-stu-id="5dabe-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="5dabe-296">Icône de bureau</span><span class="sxs-lookup"><span data-stu-id="5dabe-296">Desktop icon</span></span> | <span data-ttu-id="5dabe-297">.ico</span><span class="sxs-lookup"><span data-stu-id="5dabe-297">.ico</span></span>                                |
| <span data-ttu-id="5dabe-298">Logo de la personnalisation</span><span class="sxs-lookup"><span data-stu-id="5dabe-298">Brand logo</span></span>   | <span data-ttu-id="5dabe-299">.png</span><span class="sxs-lookup"><span data-stu-id="5dabe-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="5dabe-300">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5dabe-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dabe-301">Vue d’ensemble des styles visuels</span><span class="sxs-lookup"><span data-stu-id="5dabe-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

