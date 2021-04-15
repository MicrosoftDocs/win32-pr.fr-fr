---
description: L’interface IUpdateServiceManager définit les méthodes suivantes.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Méthodes IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525084"
---
# <a name="iupdateservicemanager-methods"></a>Méthodes IUpdateServiceManager

L’interface [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) définit les méthodes suivantes.



| Méthode                                                                           | Description                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | Inscrit un package d’analyse en tant que service avec Windows Update Agent (WUA), puis retourne une interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Inscrit un service auprès de WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Inscrit un service avec Mises à jour automatiques.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Supprime une inscription de service de WUA.                                                                                                         |
| [**SetOption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Définit des options pour l’objet qui spécifie l’ID de service, et indique s’il faut afficher un avertissement lors de la modification de l’inscription de Mises à jour automatiques. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Annule l’inscription d’un service avec Mises à jour automatiques.                                                                                                    |



 

 

 



