---
description: Types d’en-tête de bitmap
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: Types d’en-tête de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5910b0fb5be1166e807db1f3362186a206abc2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863689"
---
# <a name="bitmap-header-types"></a>Types d’en-tête de bitmap

La bitmap possède quatre types d’en-tête de base :

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

Les quatre types d’en-têtes de bitmap sont différenciés par le membre **Size** , qui est le premier **DWORD** dans chacune des structures.

La structure [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) est une structure [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) étendue, qui est une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) étendue. Toutefois, **BITMAPINFOHEADER** et [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) ont uniquement le membre **Size** en commun avec d’autres structures d’en-tête bitmap.

Les formats [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) et [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) ont été remplacés par les formats [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) et [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) , respectivement. Les formats **BITMAPCOREHEADER** et **BITMAPV4HEADER** sont présentés pour des raisons d’exhaustivité et de compatibilité descendante.

Le format d’un fichier DIB est le suivant (pour plus d’informations, consultez [stockage bitmap](bitmap-storage.md) ) :

-   une structure [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)
-   une structure [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader), [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)ou [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) .
-   une table de couleurs facultative, qui est soit un ensemble de structures [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) , soit un ensemble de structures [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) .
-   données bitmap
-   données de profil facultatives

Une table des couleurs décrit comment les valeurs de pixel correspondent aux valeurs de couleur RVB. RGB est un modèle permettant de décrire les couleurs produites en émettant de la lumière.

Les *données de profil* font référence au nom du fichier de profil (profil lié) ou aux bits du profil réel (profil incorporé). Le format de fichier place les données de profil à la fin du fichier. Les données de profil sont placées juste après la table des couleurs (le cas échéant). Toutefois, si la fonction reçoit un DIB compressé, les données de profil sont placées après les bits de la bitmap, comme dans le format de fichier.

Les données de profil existent uniquement pour les structures [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) où **BV5CSTYPE** est un profil \_ lié ou un profil \_ incorporé. Pour les fonctions qui reçoivent des DIB compactés, les données de profil sont placées après les données bitmap.

Un appareil en palette est un appareil qui utilise des palettes pour affecter des couleurs. L’exemple classique d’un appareil en palette est un affichage s’exécutant sur une profondeur de couleur de 8 bits (c’est-à-dire 256 couleurs). L’affichage dans ce mode utilise une petite table de couleurs pour assigner des couleurs à une image bitmap. Les couleurs d’une bitmap sont affectées à la couleur la plus proche dans la palette que l’appareil utilise. L’appareil en palette ne crée pas de palette optimale pour l’affichage de l’image bitmap. elle utilise simplement tout ce qui se trouve dans la palette actuelle. Les applications sont chargées de créer une palette et de la sélectionner dans le système. En général, les bitmaps 16, 24 et 32 bits par pixel (BPP) ne contiennent pas de tables de couleurs (également appelé palettes optimales pour la bitmap); dans ce cas, l’application est responsable de la génération d’une palette optimale. Toutefois, les bitmaps 16, 24 et 32-BPP peuvent contenir des tables de couleurs optimales pour l’affichage sur les appareils en palette. dans ce cas, l’application doit simplement créer une palette basée sur la table de couleurs présente dans le fichier bitmap.

Les bitmaps de 1, 4 ou 8 BPP doivent avoir une table des couleurs avec une taille maximale basée sur les BPP. La taille maximale pour les bitmaps 1, 4 et 8 bpp est 2 à la puissance des BPP. Par conséquent, une image bitmap de 1 BPP a un maximum de deux couleurs, la bitmap de 4 BPP a un maximum de 16 couleurs, et la bitmap de 8 BPP a un maximum de 256 couleurs.

Les bitmaps de 16, 24 ou 32-BPP ne nécessitent pas de tables de couleurs, mais elles peuvent spécifier des couleurs pour les appareils en palette. Si une table des couleurs est présente pour une image bitmap 16, 24 ou 32-BPP, le membre **biClrUsed** spécifie la taille de la table des couleurs et la table des couleurs doit avoir autant de couleurs. Si **biClrUsed** est égal à zéro, il n’y a aucune table de couleurs.

Les masques de champ rouge, vert et bleu pour les \_ bitmaps de champ de binaire bi suivent immédiatement les structures [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)et [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) . Les structures **BITMAPV4HEADER** et **BITMAPV5HEADER** contiennent des membres supplémentaires pour les masques rouge, vert et bleu, comme suit.



| Membre        | Signification                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | Masque de couleur qui spécifie le composant rouge de chaque pixel, valide uniquement si le membre de compression est défini sur des champs de **compression** bi \_ .   |
| **GreenMask** | Masque de couleur qui spécifie le composant vert de chaque pixel, valide uniquement si le membre de compression est défini sur des champs de **compression** bi \_ . |
| **BlueMask**  | Masque de couleur qui spécifie le composant bleu de chaque pixel, valide uniquement si le membre de compression est défini sur des champs de **compression** bi \_ .  |



 

Lorsque le membre de **bicompression** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) est défini sur des champs bi bi \_ et que la fonction reçoit un argument de type **LPBITMAPINFO**, les masques de couleur suivent immédiatement l’en-tête. La table des couleurs, le cas échéant, suivra les masques de couleur. Les bitmaps [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) ne prennent pas en charge les masques de couleur.

Par défaut, les données bitmap sont en bas au format. Bas-haut signifie que la première ligne d’analyse des données de la bitmap est la dernière ligne de numérisation à afficher. Par exemple, le 0<sup>ième</sup> pixel de la ligne d’analyse 0<sup>ième</sup> des données bitmap d’une bitmap de 10 pixels par 10 pixels correspond au 0<sup>ème</sup> pixel de la ligne de numérisation<sup>9 de</sup> l’image affichée ou imprimée. Les bitmaps de format encodés en mode d’exécution (RLE) et les bitmaps [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) ne peuvent pas être des bitmaps de haut en haut. Les lignes de numérisation sont alignées sur les **DWORD** , à l’exception des bitmaps RLE-compressés. Ils doivent être remplis pour les largeurs de ligne d’analyse, en octets, qui ne sont pas divisibles par quatre, à l’exception des bitmaps RLE compressés. Par exemple, une bitmap 10 par 10 pixels de 24 bits aura deux octets de remplissage à la fin de chaque ligne d’analyse.

 

 
