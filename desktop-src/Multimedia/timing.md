---
title: minutage (Windows multimédia)
description: Minutage
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, minutage
- DrawDibTime fonction)
- DrawDib, débogage
- débogage DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc4324de5336a00b246ad644794ce8d0b3491bb644f34e8fc22dc8a7e460ba1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688079"
---
# <a name="timing-windows-multimedia"></a>minutage (Windows multimédia)

Dans le cadre du débogage d’une application, vous pouvez obtenir des informations sur la durée nécessaire pour effectuer des opérations DrawDib répétitives. La fonction [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) retourne des informations de temporisation pour les opérations suivantes :

-   Dessin d’une image bitmap
-   Décompression d’une image bitmap
-   Tramage d’une image bitmap
-   Étirement d’une image bitmap
-   Transfert d’une bitmap à l’aide de la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)
-   Transfert d’une bitmap à l’aide de la fonction [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)

Après avoir récupéré un ensemble de valeurs, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) réinitialise le nombre et la valeur pour chaque opération.

La fonction [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) est disponible uniquement dans la version Debug des fonctions DrawDib.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’image](image-rendering.md)
</dt> </dl>

 

 
