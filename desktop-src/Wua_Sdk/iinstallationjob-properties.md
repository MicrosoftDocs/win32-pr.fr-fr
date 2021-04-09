---
description: L’interface IInstallationJob définit les propriétés suivantes.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Propriétés IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752093"
---
# <a name="iinstallationjob-properties"></a>Propriétés IInstallationJob

L’interface [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) définit les propriétés suivantes.



| Propriété                                            | Description                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Obtient l’objet d’état spécifique à l’appelant qui est passé à la méthode [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Obtient une valeur qui indique si un appel à la méthode [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) ou [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) est entièrement traité. |
| [**Mises à jour**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Obtient une interface qui contient une collection en lecture seule des mises à jour spécifiées lors de l’installation ou de la désinstallation.                                                                                                        |



 

 

 



