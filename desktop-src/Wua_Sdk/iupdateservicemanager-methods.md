---
description: L’interface IUpdateServiceManager définit les méthodes suivantes.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Méthodes IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1486727db4ed4e9b561c19a1a2f3994bca0085e836ae774fda1c7db76df38144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994349"
---
# <a name="iupdateservicemanager-methods"></a>Méthodes IUpdateServiceManager

L’interface [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) définit les méthodes suivantes.



| Méthode                                                                           | Description                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | inscrit un package d’analyse en tant que service avec Windows Update Agent (WUA), puis retourne une interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Inscrit un service auprès de WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Inscrit un service avec Mises à jour automatiques.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Supprime une inscription de service de WUA.                                                                                                         |
| [**SetOption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Définit des options pour l’objet qui spécifie l’ID de service, et indique s’il faut afficher un avertissement lors de la modification de l’inscription de Mises à jour automatiques. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Annule l’inscription d’un service avec Mises à jour automatiques.                                                                                                    |



 

 

 



