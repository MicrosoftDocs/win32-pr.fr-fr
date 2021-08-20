---
description: L’interface IUpdateService définit les propriétés suivantes.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Propriétés IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbef15c3173812f3a50d01cacba2100206f622a576a170da5a1e0a3333cebd9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106426"
---
# <a name="iupdateservice-properties"></a>Propriétés IUpdateService

L’interface [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) définit les propriétés suivantes.



| Propriété                                                              | Description                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CanRegisterWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | Obtient une valeur booléenne qui indique si le service peut s’inscrire auprès de Mises à jour automatiques.    |
| [**ContentValidationCert**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | Obtient un hachage SHA-1 du certificat utilisé pour signer le contenu du service.         |
| [**ExpirationDate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | Obtient la date à laquelle le fichier cab d’autorisation expire.                                  |
| [**IsManaged**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | Obtient une valeur booléenne qui indique si un service est un service managé.                     |
| [**IsRegisteredWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | Obtient une valeur booléenne qui indique si un service est inscrit avec Mises à jour automatiques.     |
| [**IsScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | Obtient une valeur booléenne qui indique si un service est basé sur un package d’analyse.               |
| [**Émis**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | Obtient la date à laquelle le fichier cab d’autorisation a été émis.                               |
| [**Name**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | Obtient le nom du service.                                                                   |
| [**OffersWindowsUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | obtient une valeur booléenne qui indique si le service en cours propose des mises à jour à partir de Windows mises à jour. |
| [**RedirectUrls**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | Obtient l’URL du fichier CAB du redirecteur.                                                   |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | Obtient l’identificateur d’un service.                                                              |
| [**ServiceUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | Obtient l’URL du service.                                                                   |
| [**SetupPrefix**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | Obtient le préfixe pour les fichiers d’installation.                                                            |



 

 

 



