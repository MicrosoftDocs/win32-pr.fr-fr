---
title: Redimensionnement de la boîte de dialogue acquisition de licence
description: Redimensionnement de la boîte de dialogue acquisition de licence
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Lecteur Windows Media, boîte de dialogue redimensionner l’acquisition de licence
- Lecteur Windows Media, boîte de dialogue acquisition de licence
- Lecteur Windows Media, attribut DRM_LicenseAcqURL
- boîte de dialogue Redimensionnement d’acquisition de licence
- Boîte de dialogue acquisition de licence
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380142"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Redimensionnement de la boîte de dialogue acquisition de licence

Vous pouvez ajouter des paramètres de chaîne de requête à l’URL que vous fournissez pour l’attribut **DRM \_ LicenseAcqURL** afin de spécifier une taille pour la boîte de dialogue acquisition de licence Windows Media Player 10 ou version ultérieure. Le tableau suivant répertorie les paramètres.



| Paramètre | Description                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | Spécifie la largeur de la boîte de dialogue, en pixels.  |
| *DlgY*    | Spécifie la hauteur, en pixels, de la boîte de dialogue. |



 

Par exemple, l’URL d’acquisition de licence suivante entraînerait l’ouverture de la boîte de dialogue acquisition de licence avec une taille de 800 x 600 pixels :


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



La taille maximale de la boîte de dialogue ne dépasse jamais les dimensions actuelles de l’écran moins de 20 pixels. La taille minimale est de 333 x 210 pixels (taille par défaut).

Cette fonctionnalité nécessite le lecteur Windows Media 10 ou une version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




