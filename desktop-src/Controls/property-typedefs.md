---
title: identificateurs de propriété (contrôles Windows)
description: Cette rubrique contient des informations sur les valeurs définies utilisées pour récupérer les propriétés des styles visuels. Les définitions se trouvent dans Vssym32. h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf20429d5eb5bd45ea850e3b77c5734ab6b8e0fa0e63fe4c1d2b1c918f837f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078863"
---
# <a name="property-identifiers-windows-controls"></a>identificateurs de propriété (contrôles Windows)

Cette rubrique contient des informations sur les valeurs définies utilisées pour récupérer les propriétés des styles visuels. Les définitions se trouvent dans Vssym32. h.

## <a name="property-types"></a>Types de propriétés

Le tableau suivant répertorie les types de propriété primitifs. Les valeurs de la première colonne ne sont normalement pas utilisées par les applications, mais offrent un moyen de classer les identificateurs de propriété.



| Type de données       | Description                              | Type retourné                          | Fonction de récupération                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ bool       | **True** ou **false**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| \_couleur TMT      | Valeur de couleur RVB                          | [**COLORREF**](/windows/desktop/gdi/colorref) , structure | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | Flux de disque                              | **HINSTANCE**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| \_énumération TMT       | Valeur énumérée                         | Énumération                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| \_nom de fichier TMT   | Nom de fichier relatif au répertoire du thème | Tableau **WCHAR**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| \_police TMT       | Description de la police                         | [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , structure   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ HBITMAP    | Bitmap                                   | Identificateur **HBITMAP**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ int        | Nombre signé                            | Entier                                | [**GetThemeInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint), [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint), [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| \_international TMT    | Liste d’entiers                         | Structure [**Intl**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| \_marges TMT    | Marges : à gauche, en haut, à droite et en bas    | [**Marges**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) , structure   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| \_position TMT   | Emplacement d’un élément                      | [**Point**](/previous-versions//dd162805(v=vs.85)) , structure       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ Rect       | Taille et emplacement d’un rectangle         | [**Rect**](/previous-versions//dd162897(v=vs.85)) , structure         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| taille de TMT \_       | Taille d’un élément                          | [**Taille**](/previous-versions//dd145106(v=vs.85)) de la structure         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| \_chaîne TMT     | chaîne Unicode                           | Tableau **WCHAR**                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>ID de propriété

Voici les valeurs définies pour les propriétés de thème, regroupées par type de données.

**TMT \_ bool**



| ID                        | Remarques                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | **True** si la barre de dimensionnement associée au composant et à l’État doit toujours être affichée.                                                                                                                           |
| \_REdimensionnement automatique TMT             | **True** si la zone de légende non client associée au composant et à l’État varient avec la largeur du texte.                                                                                                                 |
| TMT \_ BGFILL               | **True** si les images de taille réelle associées à la partie et à l’État doivent être dessinées sur le remplissage d’arrière-plan.                                                                                                        |
| TMT \_ BORDERONLY           | **True** si la bordure de l’image associée au composant et à l’État doit uniquement être dessinée.                                                                                                                     |
| TMT \_ composite           | **True** si le contrôle associé au composant et à l’État doit gérer sa propre composition d’images.                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| TMT \_ DRAWBORDERS          |                                                                                                                                                                                                                 |
| TMT \_ FLATMENUS            | Consultez [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| TMT \_ GLYPHONLY            | **True** si le glyphe associé au composant et à l’État doit être dessiné sans arrière-plan.                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | **True** si le glyphe associé au composant et à l’État ont des zones transparentes. Consultez [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) pour connaître la définition de la \_ valeur GLYPHCOLOR TMT qui définit la couleur transparente. |
| TMT \_ INTEGRALSIZING       | **True** si l’image truesize ou la bordure associée au composant et à l’État doivent être dimensionnées à un facteur de 2.                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **True** si l’image associée au composant et à l’État doit être retournée si la fenêtre est affichée en mode de lecture de droite à gauche.                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | **True** si l’image associée au composant et à l’État est mise à l’échelle si nécessaire.                                                                                                                |
| TMT \_ SOURCESHRINK         | **True** si l’image associée au composant et à l’État est mise à l’échelle si nécessaire.                                                                                                               |
| TMT \_ TEXTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| TMT \_ TEXTGLOW             |                                                                                                                                                                                                                 |
| TMT \_ TEXTITALIC           |                                                                                                                                                                                                                 |
| \_transparent TMT          |                                                                                                                                                                                                                 |
| TMT \_ UNIFORMSIZING        | **True** si l’image associée au composant et à l’État doit avoir la même hauteur et la même largeur.                                                                                                                      |
| TMT \_ USERPICTURE          | **True** si l’image associée au composant et à l’État est basée sur l’utilisateur actuel.                                                                                                                          |



 

**\_couleur TMT**



| ID                           | Remarques                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | Couleur utilisée comme indicateur de couleur d’accentuation pour les contrôles personnalisés.                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| \_arrière-plan TMT              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | Couleur utilisée comme couleur de fusion.                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| TMT \_ BORDERCOLOR             | Couleur de la bordure associée au composant et à l’État.                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | Couleur utilisée comme indicateur de couleur de bordure pour les contrôles personnalisés.                                                                                                                                     |
| TMT \_ BTNFACE                 |                                                                                                                                                                                                |
| TMT \_ BTNHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BTNTEXT                 |                                                                                                                                                                                                |
| TMT \_ BUTTONALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | Couleur de l’ombre foncée de l’arête associée à cette partie et à cet État.                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | Couleur de remplissage de l’arête associée à ce composant et à cet État.                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | Couleur de surbrillance de la périphérie associée à ce composant et à cet État.                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | Couleur claire de la périphérie associée à cette partie et à cet État.                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | Couleur de l’ombre de l’arête associée à ce composant et à cet État.                                                                                                                              |
| TMT \_ FILLCOLOR               | Couleur du remplissage d’arrière-plan associé au composant et à l’État.                                                                                                                           |
| TMT \_ FILLCOLORHINT           | Couleur utilisée comme indicateur de couleur de remplissage pour les contrôles personnalisés.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ GLOWCOLOR               | Couleur de la lueur produite par l’appel de [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) à l’aide de cette partie et de cet État.                                                                                    |
| TMT \_ GLYPHTEXTCOLOR          | Couleur qui sera utilisée par le glyphe basé sur la police associé à ce composant et à cet État.                                                                                                              |
| TMT \_ GLYPHTRANSPARENTCOLOR   | Couleur de glyphe transparente associée à ce composant et à cet État. Si la \_ valeur de GLYPHTRANSPARENT TMT pour cette partie et cet État est **true**, les parties du glyphe qui utilisent cette couleur ne sont pas dessinées. |
| TMT \_ GRADIENTACTIVECAPTION   |                                                                                                                                                                                                |
| TMT \_ GRADIENTCOLOR1          | Première couleur du dégradé associé à ce composant et à cet État.                                                                                                                           |
| TMT \_ GRADIENTCOLOR2          | Deuxième couleur du dégradé.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR3          | Troisième couleur du dégradé.                                                                                                                                                               |
| TMT \_ GRADIENTCOLOR4          | Quatrième couleur du dégradé.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR5          | Cinquième couleur du dégradé.                                                                                                                                                               |
| TMT \_ GRADIENTINACTIVECAPTION |                                                                                                                                                                                                |
| TMT \_ GRAYTEXT                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| TMT en \_ surbrillance               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| TMT \_ HOTTRACKING             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ InfoText                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| \_menu TMT                    |                                                                                                                                                                                                |
| \_barre de menus TMT                 |                                                                                                                                                                                                |
| TMT \_ MENUHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| TMT \_ ScrollBar               |                                                                                                                                                                                                |
| TMT \_ SHADOWCOLOR             | Couleur de l’ombre dessinée sous le texte associé à ce composant et à cet État.                                                                                                             |
| TMT \_ TEXTBORDERCOLOR         | Couleur de la bordure de texte associée à ce composant et à cet État.                                                                                                                              |
| TMT \_ TEXTCOLOR               | Couleur du texte associé à ce composant et à cet État.                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | Couleur de l’ombre de texte associée à ce composant et à cet État.                                                                                                                              |
| TMT \_ transparente        | Couleur transparente associée à ce composant et à cet État. Si la \_ valeur transparente TMT pour cette partie et cet État est **true**, les parties du graphique qui utilisent cette couleur ne sont pas dessinées.          |
| \_fenêtre TMT                  |                                                                                                                                                                                                |
| TMT \_ WINDOWFRAME             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| ID              | Remarques |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**\_énumération TMT**



| Énumération         | Valeurs de la propriété                                                                                                                                                                                                                                            | Remarques                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | \_image BT, BT \_ BORDERFILL                                                                                                                                                                                                                              | Type de dessin de base pour ce composant.                                                                                                                |
| BORDERTYPE          | BT \_ Rect, BT \_ ROUNDRECT, \_ ellipses BT                                                                                                                                                                                                                       | Type de bordure dessinée si cette partie est un remplissage de bordure.                                                                                              |
| CONTENTALIGNMENT    | AUTORITÉ \_ de certification gauche, \_ Centre de l’autorité de certification, \_ droit AC                                                                                                                                                                                                                            | Alignement du texte dans la légende associée à ce composant.                                                                                      |
| FILLTYPE            | FT \_ Solid, ft \_ VERTGRADIENT, ft \_ HORZGRADIENT, FT \_ RADIALGRADIENT, ft \_ TILEIMAGE                                                                                                                                                                           | Type de forme de remplissage dessiné si cette partie est un remplissage de bordure.                                                                                          |
| GLYPHTYPE           | GT \_ None, gt \_ IMAGEGLYPH, gt \_ FONTGLYPH                                                                                                                                                                                                                    | Type de glyphe dessiné sur ce composant.                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ None, GFST \_ Size, GFST \_ dpi                                                                                                                                                                                                                          | Type de méthode utilisé pour sélectionner des glyphes de taille différente.                                                                                    |
| HALIGN              | haute disponibilité HA \_ , \_ Centre HA, ha \_ droit                                                                                                                                                                                                                            | Alignement horizontal si cette partie utilise une image de taille réelle.                                                                                        |
| ICONEFFECT          | ICE \_ None, lueur glacée, Shadow Ice, Ice Ice \_ \_ \_ , Ice \_ alpha                                                                                                                                                                                                  | Type d’effet à afficher lorsque cette partie est dessinée à l’aide de [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                             |
| IMAGELAYOUT         | IL \_ vertical, il \_ horizontal                                                                                                                                                                                                                               | Type d’alignement utilisé lorsque plusieurs images sont dessinées.                                                                                           |
| IMAGESELECTTYPE     | TSI \_ None, \_ taille TSI, TSI \_ dpi                                                                                                                                                                                                                             | Type de méthode permettant de sélectionner les images de taille pour ce composant. Consultez la \_ valeur TMT IMAGEFILE1 de [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OFFSETTYPE          | OT- \_ Left, OT- \_ Right, OT- \_ Middle, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, OT \_ MIDDLERIGHT, OT \_ LEFTOFCAPTION, OT RIGHTOFCAPTION \_ , OT LEFTOFLASTBUTTON, OT \_ \_ RIGHTOFLASTBUTTON, OT ABOVELASTBUTTON \_ , OT \_ BELOWLASTBUTTON | Alignement de cette partie sur la fenêtre.                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE, St \_ Stretch, Saint \_ Tile, St \_ TILEHORZ, St \_ TILEVERT, St \_ TILECENTER                                                                                                                                                                            | Méthode utilisée pour dimensionner une image si cette partie utilise un fichier image.                                                                                    |
| TEXTSHADOWTYPE      | TST \_ aucun, TST \_ unique, TST \_ continu                                                                                                                                                                                                                    | Type d’effet d’ombre pour dessiner derrière le texte associé à ce composant.                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ None, TSST \_ Size, TSST \_ dpi                                                                                                                                                                                                                          | Type de mise à l’échelle utilisé si cette partie utilise une image de taille réelle.                                                                                       |
| VALIGN              | VA du \_ haut, \_ Centre VA, va en \_ bas                                                                                                                                                                                                                            | Alignement vertical si cette partie utilise une image de taille réelle.                                                                                          |



 

**\_nom de fichier TMT**



| ID                  | Remarques                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYPHIMAGEFILE | Nom de fichier de l’image de glyphe associée à ce composant et à cet État.                                                                        |
| \_image TMT      | Nom de fichier de l’image associée à ce composant et à cet État, ou nom de fichier de base pour plusieurs images associées à ce composant et à cet État. |
| TMT \_ IMAGEFILE1     | Nom de fichier de la première image mise à l’échelle associée à cette partie et à cet État, pour la prise en charge de différentes résolutions.                            |
| TMT \_ IMAGEFILE2     | Nom de fichier de la deuxième image mise à l’échelle.                                                                                                     |
| TMT \_ IMAGEFILE3     | Nom de fichier de la troisième image mise à l’échelle.                                                                                                      |
| TMT \_ IMAGEFILE4     | Nom de fichier de la quatrième image mise à l’échelle.                                                                                                     |
| TMT \_ IMAGEFILE5     | Nom de fichier de la cinquième image mise à l’échelle.                                                                                                      |



 

**\_police TMT**



| ID                    | Remarques                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| TMT \_ GLYPHFONT        | Police avec laquelle le glyphe associé à ce composant sera dessiné, si des glyphes basés sur la police sont utilisés. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| TMT \_ ICONTITLEFONT    |                                                                                                      |
| TMT \_ MENUFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| TMT \_ STATUSFONT       |                                                                                                      |



 

**TMT \_ int**



| ID                       | Remarques                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | Valeur alpha (0-255) utilisée pour [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | Valeur alpha minimale (0-255) qu’un pixel doit avoir pour être considéré comme opaque.                                                                                                                                  |
| TMT \_ ANIMATIONDELAY      |                                                                                                                                                                                                                  |
| TMT \_ ANIMATIONDURATION   |                                                                                                                                                                                                                  |
| TMT de \_ bordure          | Épaisseur de la bordure dessinée si cette partie utilise un remplissage de bordure.                                                                                                                                               |
| jeu de caractères TMT \_             |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONCOLOR   |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONOPACITY |                                                                                                                                                                                                                  |
| TMT \_ FRAMESPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT \_ GLOWINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | Index de caractère dans la police sélectionnée qui sera utilisée pour le glyphe, si la partie utilise un glyphe basé sur la police.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | Quantité de la première couleur de dégradé (TMT \_ GRADIENTCOLOR1) à utiliser pour dessiner la partie. Cette valeur peut être comprise entre 0 et 255, mais cette valeur plus les valeurs de chacune des valeurs GRADIENTRATIO doivent être additionnées à 255. |
| TMT \_ GRADIENTRATIO2      | Quantité de la deuxième couleur de dégradé (TMT \_ GRADIENTCOLOR2) à utiliser pour dessiner la partie.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | Quantité de la troisième couleur de dégradé (TMT \_ GRADIENTCOLOR3) à utiliser pour dessiner la partie.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | Quantité de la quatrième couleur de dégradé (TMT \_ GRADIENTCOLOR4) à utiliser pour dessiner la partie.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | Quantité de la cinquième couleur de dégradé (TMT \_ GRADIENTCOLOR5) à utiliser pour dessiner la partie.                                                                                                                         |
| hauteur de TMT \_              | Hauteur du composant.                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | Nombre d’images d’État présentes dans un fichier image.                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | Nombre minimal de points par pouce (dpi) pour lesquels le premier fichier image a été conçu.                                                                                                                                      |
| TMT \_ MINDPI2             | Résolution minimale pour laquelle le deuxième fichier image a été conçu.                                                                                                                                                     |
| TMT \_ MINDPI3             | Résolution minimale pour laquelle le troisième fichier image a été conçu.                                                                                                                                                      |
| TMT \_ MINDPI4             | Résolution minimale pour laquelle le quatrième fichier image a été conçu.                                                                                                                                                     |
| TMT \_ MINDPI5             | Résolution minimale pour laquelle le cinquième fichier image a été conçu.                                                                                                                                                      |
| \_opacité TMT             |                                                                                                                                                                                                                  |
| TMT \_ PIXELSPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | Taille des formes « Chunk » du contrôle de progression qui définissent la progression d’une opération.                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | Taille totale de l’ensemble des « segments » du contrôle de progression.                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | Arrondi (de 0 à 100 pour cent) des angles du composant.                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | Arrondi (de 0 à 100 pour cent) des angles du composant.                                                                                                                                                          |
| \_saturation TMT          | La quantité de saturation (0-255) à appliquer à une icône dessinée à l’aide de [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                         |
| TMT \_ TEXTBORDERSIZE      | Épaisseur de la bordure dessinée autour des caractères de texte.                                                                                                                                                        |
| TMT \_ TEXTGLOWSIZE        |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR1            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR2            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR3            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR4            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR5            |                                                                                                                                                                                                                  |
| TMT \_ TOHUE1              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE2              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE3              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE4              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE5              |                                                                                                                                                                                                                  |
| TMT \_ TRUESIZESTRETCHMARK | Pourcentage de la taille d’origine de l’image de taille réelle à laquelle l’image sera étirée.                                                                                                                        |
| largeur de TMT \_               | Largeur du composant.                                                                                                                                                                                           |



 

**\_international TMT**



| ID                       | Remarques |
|--------------------------|-------|
| TMT \_ TRANSITIONDURATIONS |       |



 

**\_marges TMT**



| ID                  | Remarques                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | Marges qui définissent où le texte de légende peut être placé dans un composant. |
| TMT \_ CONTENTMARGINS | Marges qui définissent où le contenu peut être placé dans un composant.      |
| TMT \_ SIZINGMARGINS  | Marges utilisées pour le dimensionnement d’une image de taille non vraie.                      |



 

**\_position TMT**



| ID                    | Remarques                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MinSize          | Taille minimale pour laquelle le fichier image normal peut être utilisé avant de passer au plus petit fichier image suivant.   |
| TMT \_ MINSIZE1         | Taille minimale pour laquelle le premier petit fichier image peut être utilisé.                                            |
| TMT \_ MINSIZE2         | Taille minimale pour laquelle le deuxième petit fichier image peut être utilisé.                                           |
| TMT \_ MINSIZE3         | Taille minimale pour laquelle le troisième petit fichier image peut être utilisé.                                            |
| TMT \_ MINSIZE4         | Taille minimale pour laquelle le quatrième petit fichier image peut être utilisé.                                           |
| TMT \_ MINSIZE5         | Taille minimale pour laquelle le cinquième fichier image peut être utilisé.                                            |
| TMT \_ NORMALSIZE       | Taille de l’image normale associée à ce composant.                                                      |
| \_décalage TMT           | Décalage de position par rapport à l’alignement pour ce composant. L’alignement est défini par la \_ valeur OFFSETTYPE TMT. |
| TMT \_ TEXTSHADOWOFFSET | Décalage à partir du texte auquel les ombres du texte sont dessinées.                                                    |



 

**TMT \_ Rect**



| ID                       | Remarques                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| TMT \_ CUSTOMSPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | Taille par défaut du composant. |



 

**taille de TMT \_**



| ID                      | Remarques                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | Hauteur de la barre de légende.       |
| TMT \_ CAPTIONBARWIDTH    | Largeur de la barre de légende.        |
| TMT \_ MENUBARHEIGHT      | Hauteur de la barre de menus.          |
| TMT \_ MENUBARWIDTH       | Largeur de barre de menus.           |
| TMT \_ PADDEDBORDERWIDTH  | Largeur de bordure remplie.      |
| TMT \_ SCROLLBARHEIGHT    | Hauteur de la barre de défilement.        |
| TMT \_ SCROLLBARWIDTH     | Largeur de barre de défilement.         |
| TMT \_ SIZINGBORDERWIDTH  | Largeur d’une bordure de redimensionnement. |
| TMT \_ SMCAPTIONBARHEIGHT | Hauteur de la barre de légende.       |
| TMT \_ SMCAPTIONBARWIDTH  | Largeur de la barre de légende.        |



 

**\_chaîne TMT**



| ID                   | Remarques                                               |
|----------------------|-----------------------------------------------------|
| \_alias TMT           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| \_auteur TMT          |                                                     |
| TMT \_ CLASSICVALUE    |                                                     |
| TMT \_ COLORSCHEMES    |                                                     |
| \_entreprise TMT         |                                                     |
| \_Copyright TMT       |                                                     |
| TMT \_ CSSNAME         | Consultez [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| Description de TMT \_     |                                                     |
| TMT \_ DisplayName     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| tailles de TMT \_           |                                                     |
| \_texte TMT            | Texte affiché par le composant.                     |
| \_info-bulle TMT         |                                                     |
| \_URL TMT             |                                                     |
| VERSION de TMT \_         |                                                     |
| TMT \_ XMLNAME         | Consultez [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| nom de TMT \_            |                                                     |



 

 

 
