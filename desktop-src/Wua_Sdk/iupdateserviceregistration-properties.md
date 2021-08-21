---
description: L’interface IUpdateServiceRegistration définit les propriétés suivantes.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Propriétés IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824f76c01b428d156d12752d07bb9547517df26a0e621f44a701e94f33340221
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814807"
---
# <a name="iupdateserviceregistration-properties"></a>Propriétés IUpdateServiceRegistration

L’interface **IUpdateServiceRegistration** définit les propriétés suivantes.



| Propriété                                                                                      | Description                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsPendingRegistrationWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | Obtient une valeur booléenne qui indique si le service est également inscrit avec Mises à jour automatiques, lorsqu’il est ajouté.                                  |
| [**RegistrationState**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | Obtient une valeur [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) qui indique l’état actuel de l’inscription du service. |
| [**Service**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | Obtient un pointeur vers une interface [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) . Cette propriété est la propriété par défaut.                                    |



 

 

 



