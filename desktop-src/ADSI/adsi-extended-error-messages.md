---
title: Messages d’erreur étendus ADSI
description: Cette rubrique contient une liste de rubriques qui expliquent comment utiliser les messages d’erreur ADSI retournés par IADs, IADsContainer, IDirectoryObject et IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Messages d’erreur étendus ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2bf4c7faef20feeb868fdcbb0e36d7f1ad5d0b9c68cc8879d5019e81e186a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180873"
---
# <a name="adsi-extended-error-messages"></a>Messages d’erreur étendus ADSI

Outre les valeurs **HRESULT** , plusieurs fournisseurs de système ADSI (principalement LDAP) renvoient des données d’erreur supplémentaires pour les opérations effectuées par les interfaces suivantes :

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**Rubrique IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Une partie de ces données d’erreur étendues est la chaîne envoyée par le serveur dans le cadre du résultat du message.

Appelez [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) pour récupérer ces messages d’erreur étendus. Le premier paramètre de cette fonction, *lpError*, est une valeur **DWORD** . Pour un serveur Active Directory, ADSI tente de mapper un message d’erreur LDAP à un code d’erreur Win32 approprié et attribue la valeur de code d’erreur Win32 à *lpError*. Si le mappage n’est pas résolu, ADSI affecte des **\_ \_ données non valides** à *lpError*, comme c’est le cas pour tout autre serveur d’annuaire. Dans tous les cas, ADSI relaie fidèlement la chaîne de la description d’erreur du serveur au client par le biais de *lpErrorBuf*, le deuxième paramètre de la fonction **ADsGetLastError** .

 

 




