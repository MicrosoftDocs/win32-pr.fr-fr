---
description: Pour permettre aux applications de placer la sortie en mémoire au lieu de l’envoyer à un appareil réel, utilisez un contexte de périphérique spécial pour les opérations de bitmap appelée « contexte de périphérique de mémoire ».
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Contextes de périphérique mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095de04fdf965a87011895015ad7ea6c9782e286
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415943"
---
# <a name="memory-device-contexts"></a>Contextes de périphérique mémoire

Pour permettre aux applications de placer la sortie en mémoire au lieu de l’envoyer à un appareil réel, utilisez un contexte de périphérique spécial pour les opérations de bitmap appelée « *contexte de périphérique de mémoire*». Un contrôleur de réseau permet au système de traiter une partie de la mémoire en tant qu’appareil virtuel. Il s’agit d’un tableau de bits en mémoire qu’une application peut utiliser temporairement pour stocker les données de couleur pour les bitmaps créées sur une surface de dessin normale. Étant donné que la bitmap est compatible avec l’appareil, un contrôleur de périphérique de mémoire est également parfois désigné comme un *contexte de périphérique compatible*.

Le DC de mémoire stocke des images bitmap pour un appareil particulier. Une application peut créer un DC de mémoire en appelant la fonction [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) .

Le bitmap d’origine dans un contrôleur de périphérique de mémoire est simplement un espace réservé. Ses dimensions sont d’un pixel par pixel. Avant qu’une application puisse commencer à dessiner, elle doit sélectionner une image bitmap avec la largeur et la hauteur appropriées dans le DC en appelant la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Pour créer une image bitmap des dimensions appropriées, utilisez la fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) . Une fois que l’image bitmap est sélectionnée dans le DC de mémoire, le système remplace le tableau à un seul bit par un tableau suffisamment grand pour stocker les informations de couleur du rectangle de pixels spécifié.

Quand une application transmet le descripteur renvoyé par [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) à l’une des fonctions de dessin, la sortie demandée n’apparaît pas sur la surface de dessin d’un appareil. Au lieu de cela, le système stocke les informations de couleur de la ligne, de la courbe, du texte ou de la région qui en résulte dans le tableau de bits. L’application peut copier l’image stockée en mémoire sur une surface de dessin en appelant la fonction [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , en identifiant le DC de mémoire comme contexte de périphérique source et en tant que contexte de périphérique cible comme contexte de périphérique cible.

Lorsque vous affichez un DIB ou un DDB créé à partir d’un DIB sur un appareil de palette, vous pouvez améliorer la vitesse à laquelle l’image est dessinée en réorganisant la palette logique pour qu’elle corresponde à la disposition de la palette système. Pour ce faire, appelez [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) avec la valeur NUMRESERVED pour connaître le nombre de couleurs réservées dans le système. Appelez ensuite [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) et renseignez les première et dernière entrées NUMRESERVED/2 de la palette logique avec les couleurs système correspondantes. Par exemple, si NUMRESERVED est défini sur 20, vous devez remplir les 10 premières et dernières entrées de la palette logique avec les couleurs système. Renseignez ensuite les couleurs 256-NUMRESERVED restantes de la palette logique (dans notre exemple, les 236 autres couleurs) avec des couleurs du DIB et définissez l' \_ indicateur NOcollapse du PC sur chacune de ces couleurs.

Pour plus d’informations sur les couleurs et les palettes, consultez [couleurs](colors.md). Pour plus d’informations sur les bitmaps et les opérations de bitmap, consultez [bitmaps](bitmaps.md).

 

 



