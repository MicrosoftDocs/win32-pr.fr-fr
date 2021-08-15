---
description: L’interface IUpdateDownloader définit les propriétés suivantes.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propriétés IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf66fbdad678ef6a78d0fa049ecb59c34be2ca9d08c873e24e82c35c9d1eb1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738288"
---
# <a name="iupdatedownloader-properties"></a>Propriétés IUpdateDownloader

L’interface [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) définit les propriétés suivantes.



| Propriété                                                             | Description                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Obtient et définit l’application cliente actuelle.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | obtient et définit une valeur booléenne qui indique si l’Agent de Windows Update (WUA) force le téléchargement des mises à jour déjà installées ou qui ne peuvent pas être installées. |
| [**Priorité**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Obtient et définit le niveau de priorité du téléchargement.                                                                                                                          |
| [**Mises à jour**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Obtient et définit une interface qui contient une collection en lecture seule des mises à jour spécifiées pour le téléchargement.                                                            |



 

 

 



