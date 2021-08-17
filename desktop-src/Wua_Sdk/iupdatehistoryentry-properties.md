---
description: L’interface IUpdateHistoryEntry définit les propriétés suivantes.
ms.assetid: ea4e698c-4a4c-4266-96e0-870dc5709a72
title: Propriétés IUpdateHistoryEntry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5c6951857f72f4a9ee4f86cd29d42e024e05b87d58d589043f5a40e951d4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738268"
---
# <a name="iupdatehistoryentry-properties"></a>Propriétés IUpdateHistoryEntry

L’interface [**IUpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry) définit les propriétés suivantes.



| Propriété                                                               | Description                                                                                                              |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_clientapplicationid) | Obtient l’identificateur de l’application cliente qui a traité une mise à jour.                                                  |
| [**Date**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_date)                               | Obtient la date et l’heure auxquelles une mise à jour a été appliquée.                                                                        |
| [**Description**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_description)                 | Obtient la description d’une mise à jour.                                                                                       |
| [**Signé**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_hresult)                         | Obtient la valeur **HRESULT** retournée par l’opération sur une mise à jour.                                             |
| [**Opération**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_operation)                     | Obtient une valeur [**Update**](/windows/win32/api/wuapi/ne-wuapi-updateoperation) qui spécifie l’opération sur une mise à jour.                      |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_resultcode)                   | Obtient une valeur [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) qui spécifie le résultat d’une opération sur une mise à jour. |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serverselection)         | Obtient la valeur [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) qui indique le serveur qui a fourni une mise à jour.                |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_serviceid)                     | obtient l’identificateur de service d’un service de mise à jour qui n’est pas une mise à jour Windows.                                           |
| [**SupportUrl**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_supporturl)                   | Obtient un lien hypertexte vers les informations de prise en charge spécifiques au langage pour une mise à jour.                                             |
| [**Titre**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_title)                             | Obtient le titre d’une mise à jour.                                                                                             |
| [**UninstallationNotes**](/windows/win32/api/wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationnotes) | Obtient les notes de désinstallation d’une mise à jour.                                                                              |
| [**UninstallationSteps**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_uninstallationsteps) | Obtient l’interface [**IStringCollection**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection) qui contient les étapes de désinstallation d’une mise à jour.  |
| [**UnmappedResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_unmappedresultcode)   | Obtient le code de résultat non mappé qui est retourné à partir d’une opération sur une mise à jour.                                           |
| [**UpdateIdentity**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatehistoryentry-get_updateidentity)           | Obtient une chaîne. La chaîne contient l’identificateur unique d’une mise à jour.                                                   |



 

 

 
