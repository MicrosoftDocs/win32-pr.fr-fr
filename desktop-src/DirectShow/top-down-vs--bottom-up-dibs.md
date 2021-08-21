---
description: Top-Down et
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down et Bottom-Up DIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff1d525423ef8590a3656a5e63f7541be180e2dcc5c70307f93298eb9ce991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951564"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down et Bottom-Up DIB

Si vous ne connaissez pas la programmation graphique, vous pouvez vous attendre à ce qu’une bitmap soit organisée en mémoire afin que la ligne supérieure de l’image apparaisse au début de la mémoire tampon, suivie de la ligne suivante, et ainsi de suite. Toutefois, cela n’est pas nécessairement le cas. dans Windows, les bitmaps indépendantes du périphérique (dib) peuvent être placées en mémoire dans deux orientations différentes, de bas en haut et de haut en bas.

Dans un DIB de bas en haut, la mémoire tampon d’image commence par la ligne inférieure des pixels, suivie de la ligne suivante, et ainsi de suite. La ligne supérieure de l’image est la dernière ligne de la mémoire tampon. Par conséquent, le premier octet en mémoire est le pixel inférieur gauche de l’image. Dans GDI, tous les DIB sont ascendants. Le diagramme suivant montre la disposition physique d’un DIB ascendant.

![DIB ascendant](images/pixel-layout-bottomup.png)

Dans un DIB descendant, l’ordre des lignes est inversé. La ligne supérieure de l’image est la première ligne en mémoire, suivie de la ligne suivante. La ligne inférieure de l’image est la dernière ligne de la mémoire tampon. Avec un DIB descendant, le premier octet en mémoire est le pixel supérieur gauche de l’image. DirectDraw utilise des DIB descendants. Le diagramme suivant montre la disposition physique d’un DIB descendant :

![DIB descendant](images/pixel-layout-topdown.png)

Pour les DIB RGB, l’orientation de l’image est indiquée par le membre **biheight** de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Si la **bihauteur** est positive, l’image est en bas. Si la **bihauteur** est négative, l’image est de haut en haut.

Les DIB dans les formats YUV sont toujours de haut en haut et le signe du membre **biheight** est ignoré. Les décodeurs doivent offrir des formats YUV avec une **bihauteur** positive, mais ils doivent également accepter les formats YUV avec une **bihauteur** négative et ignorer le signe.

En outre, tout type DIB qui utilise un **FourCC** dans le membre de **bicompression** doit exprimer sa **bihauteur** sous la forme d’un nombre positif, quelle que soit son orientation, puisque le **FourCC** lui-même identifie un schéma de compression dont l’orientation d’image doit être comprise par n’importe quel filtre compatible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des images vidéo](working-with-video-frames.md)
</dt> </dl>

 

 



