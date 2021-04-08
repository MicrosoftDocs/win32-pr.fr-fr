---
description: L’interface IUpdateDownloader définit les propriétés suivantes.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propriétés IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752084"
---
# <a name="iupdatedownloader-properties"></a>Propriétés IUpdateDownloader

L’interface [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) définit les propriétés suivantes.



| Propriété                                                             | Description                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | Obtient et définit l’application cliente actuelle.                                                                                                                              |
| [**IsForced**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | Obtient et définit une valeur booléenne qui indique si l’agent de Windows Update (WUA) force le téléchargement des mises à jour déjà installées ou qui ne peuvent pas être installées. |
| [**Priorité**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | Obtient et définit le niveau de priorité du téléchargement.                                                                                                                          |
| [**Mises à jour**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | Obtient et définit une interface qui contient une collection en lecture seule des mises à jour spécifiées pour le téléchargement.                                                            |



 

 

 



