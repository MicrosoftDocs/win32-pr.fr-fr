---
description: Interface implémentée par le client qui permet aux développeurs de fournir leurs propres informations d’identification de manière dynamique au moment de l’exécution pour authentifier les conteneurs non joints à un domaine avec Active Directory.
title: Interface ICcgDomainAuthCredentials (ccgplugins. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106545869"
---
# <a name="iccgdomainauthcredentials-interface"></a>Interface ICcgDomainAuthCredentials

Interface implémentée par le client qui permet aux développeurs de fournir leurs propres informations d’identification de manière dynamique au moment de l’exécution pour authentifier les conteneurs non joints à un domaine avec Active Directory. 

## <a name="members"></a>Membres

L’interface **ICcgDomainAuthCredentials** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ICcgDomainAuthCredentials** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ICcgDomainAuthCredentials** possède ces méthodes.



| Méthode                                           | Description                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetPasswordCredentials**](iccgdomainauthcredentials-getpasswordcredentials.md)               | Retourne les informations d’identification pour authentifier un conteneur non joint à un domaine avec Active Directory.<br/>                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>ccgplugins. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>ccgplugins. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ccgplugins.dll</dt> </dl> |
| IID<br/>                      | 6ecda518-2010-4437-8bc3-46e752b7b172<br/>          |



 

