---
title: Redimensionnement de la boîte de dialogue acquisition de licence
description: Redimensionnement de la boîte de dialogue acquisition de licence
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Lecteur Windows Media, boîte de dialogue redimensionnement d’Acquisition de licence
- Lecteur Windows Media, boîte de dialogue Acquisition de licence
- Lecteur Windows Media, DRM_LicenseAcqURL attribut
- boîte de dialogue Redimensionnement d’acquisition de licence
- Boîte de dialogue acquisition de licence
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416192"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a>Redimensionnement de la boîte de dialogue acquisition de licence

vous pouvez ajouter des paramètres de chaîne de requête à l’URL que vous fournissez pour l’attribut **DRM \_ LicenseAcqURL** afin de spécifier une taille pour la boîte de dialogue d’acquisition de licence Lecteur Windows Media 10 ou version ultérieure. Le tableau suivant répertorie les paramètres.



| Paramètre | Description                                        |
|-----------|----------------------------------------------------|
| *DlgX*    | Spécifie la largeur de la boîte de dialogue, en pixels.  |
| *DlgY*    | Spécifie la hauteur, en pixels, de la boîte de dialogue. |



 

Par exemple, l’URL d’acquisition de licence suivante entraînerait l’ouverture de la boîte de dialogue acquisition de licence avec une taille de 800 x 600 pixels :


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



La taille maximale de la boîte de dialogue ne dépasse jamais les dimensions actuelles de l’écran moins de 20 pixels. La taille minimale est de 333 x 210 pixels (taille par défaut).

cette fonctionnalité nécessite Lecteur Windows Media 10 ou version ultérieure.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




