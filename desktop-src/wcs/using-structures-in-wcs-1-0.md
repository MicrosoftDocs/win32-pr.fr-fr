---
title: Utilisation de structures dans WCS 1.0
description: La plupart des structures utilisées par WCS 1,0 sont très simples et nécessitent peu d’explications. Elles sont documentées dans la section de référence du WCS 1,0 structures d’intitulé.
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Système de couleurs Windows (WCS), structures
- WCS (système de couleurs Windows), structures
- gestion des couleurs des images, structures
- gestion des couleurs, structures
- couleurs, structures
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531264"
---
# <a name="using-structures-in-wcs-10"></a>Utilisation de structures dans WCS 1.0

La plupart des structures utilisées par WCS 1,0 sont très simples et nécessitent peu d’explications. Elles sont documentées dans la section de référence du WCS 1,0 [structures](structures.md)d’intitulé.

Les exceptions sont la structure [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw) utilisée par la fonction [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) , et les structures Windows suivantes définies dans WinGDI. h :

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIEXYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**CIEXYZTRIPLE**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

Les rubriques suivantes sont traitées de façon plus longue :

-   [Structures d’en-tête bitmap Windows](#windows-bitmap-header-structures)
-   [Différences entre les en-têtes V4 et v5](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe : utilitaire Command-Line pour la conversion d’en-têtes bitmap](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Structures d’en-tête bitmap Windows

WCS 1,0 permet de lier ou d’incorporer les profils de couleurs ICC dans des bitmaps indépendantes du périphérique (DIB). Cela permet de caractériser les couleurs DIB de manière plus précise que si vous utilisiez WCS dans Windows 95. [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) , la nouvelle structure d’en-tête bitmap, est définie dans WinGDI. h dans la version de Windows 98. À des fins de développement, il est également inclus dans le fichier ICM. h avec ce guide de référence du programmeur. La structure **BITMAPV5HEADER** est la suivante :


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



Le **bV5CSType** membre peut avoir le profil des valeurs \_ incorporé ou le profil \_ lié pour spécifier si un profil est incorporé ou lié au dib. Le membre **bV5ProfileData** est le décalage, en octets, entre le début de la structure **BITMAPV5HEADER** et le début des données de profil. Si le profil est incorporé, les données de profil sont le profil réel et, s’il est lié, les données de profil sont le nom de fichier se terminant par un caractère null du profil. Il ne peut pas s’agir d’une chaîne Unicode. Elle doit être composée exclusivement de caractères à partir du jeu de caractères Windows (page de codes 1252).

Lorsqu’un DIB est chargé en mémoire, les données de profil (le cas échéant) doivent suivre la table des couleurs, et **bV5ProfileData** doit donner le décalage des données de profil à partir du début de la structure **BITMAPV5HEADER** . La valeur de ce membre sera maintenant différente, car les bits de la bitmap ne suivent pas la table des couleurs en mémoire. Les applications doivent modifier le membre **bV5ProfileData** après le chargement du DIB dans la mémoire.

Pour les fichiers DIB compactés, les données de profil doivent suivre les bits de bitmap similaires au format de fichier. Le membre **bV5ProfileData** doit toujours fournir le décalage des données de profil à partir du début de la structure **BITMAPV5HEADER** .

Les applications doivent accéder aux données de profil uniquement quand **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** est un profil \_ incorporé ou un profil \_ lié.

Si un profil est lié, le chemin d’accès du profil peut être n’importe quel nom complet (y compris un chemin d’accès réseau) qui peut être ouvert à l’aide de la fonction **CreateFile** de Win32.

## <a name="differences-between-v4-and-v5-headers"></a>Différences entre les en-têtes V4 et v5

Dans l’utilisation de la nouvelle structure bitmap, il est utile de reconnaître les différences de configuration des structures **BITMAPV4HEADER** et **BITMAPV5HEADER** :



| En-tête v4     | Signification                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | \_ \_ RGB étalonné. Cette valeur implique que les points de terminaison et les gammas sont fournis dans les champs appropriés. Des valeurs erronées provoquent des problèmes. |
| **bV4CSType** | SRGB de LCS \_ . Cette valeur implique que la bitmap se trouve dans l’espace de couleurs sRVB (gammas et points de terminaison ignorés).                                 |
| **bV4CSType** | \_espace de \_ couleurs Windows LCS \_ . Cette valeur implique que la bitmap se trouve dans l’espace de couleurs Windows par défaut.                                    |



 



| En-tête v5     | Signification                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | \_ \_ RGB étalonné. Cette valeur implique que les points de terminaison et les gammas sont fournis dans les champs appropriés. Des valeurs erronées provoquent des problèmes.                         |
| **bV5CSType** | SRGB de LCS \_ . Cette valeur implique que la bitmap se trouve dans l’espace de couleurs sRVB (gammas et points de terminaison ignorés).                                                         |
| **bV5CSType** | Profil \_ incorporé. Cette valeur implique que **bV5ProfileData** pointe vers une mémoire tampon qui contient le profil à utiliser (les valeurs gamma et les points de terminaison sont ignorés). |
| **bV5CSType** | Profil \_ lié. Cette valeur implique que **bV5ProfileData** pointe vers le nom de fichier du profil à utiliser (les valeurs gamma et les points de terminaison sont ignorés).                |
| **bV5CSType** | \_espace de \_ couleurs Windows LCS \_ . Cette valeur implique que la bitmap se trouve dans l’espace de couleurs Windows par défaut.                                                            |



 

Pour convertir les bitmaps plus anciennes vers et à partir de la nouvelle structure **BITMAPV5HEADER** , un fichier utilitaire de conversion de ligne de commande nommé Bitmap.exe est inclus dans le Guide de référence du programmeur WCS 1,0.

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe : utilitaire Command-Line pour la conversion d’en-têtes bitmap

Bitmap.exe est un utilitaire de ligne de commande situé dans le \\ dossier bin sous le dossier d’installation que vous avez spécifié. Il modifie les en-têtes des bitmaps Windows, ce qui vous permet de convertir les bitmaps existantes des structures d’en-tête **BITMAPINFOHEADER** et **BITMAPV4HEADER** vers la nouvelle structure **BITMAPV5HEADER** , puis de les replacer. La syntaxe de la ligne de commande est la suivante :


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



Les commutateurs de ligne de commande ont les effets suivants.



| Commutateur | Signification                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | Les valeurs par défaut sont automatiquement entrées dans les en-têtes convertis.       |
| /1     | Convertir les bitmaps spécifiées en **BITMAPINFOHEADER**                    |
| /4     | Convertir les bitmaps spécifiées en **BITMAPV4HEADER**                      |
| /5     | Convertir les bitmaps spécifiées en **BITMAPV5HEADER**                      |
| /f     | Force la conversion, même si la bitmap a déjà l’en-tête de droite       |
| /s     | Convertit les bitmaps dans le dossier spécifié et tous les sous-répertoires qu’il contient |



 

 

 