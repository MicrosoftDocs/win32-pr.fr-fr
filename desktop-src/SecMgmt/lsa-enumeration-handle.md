---
description: "Le type de données du handle de l' \\_ énumération LSA \\_ est utilisé par la fonction LSA qui énumère les objets trustedDomain : LsaEnumerateTrustedDomainsEx."
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324736"
---
# <a name="lsa_enumeration_handle"></a>\_handle d’énumération LSA \_

Le type de données du handle de l' **\_ énumération \_ LSA** est utilisé par la fonction LSA qui énumère les objets [**trustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex). Cette fonction est conçue afin que vous puissiez effectuer plusieurs appels pour énumérer tous les objets d’un type donné dans la base de données.

Lors de l’appel initial de la fonction d’énumération, vous transmettez un pointeur vers une variable de **\_ \_ handle d’énumération LSA** qui est initialisée à zéro. La fonction met à jour cette valeur. Si la fonction retourne une valeur qui indique qu’il y a plus d’objets à énumérer, appelez à nouveau la fonction et transmettez la valeur de **\_ \_ handle d’énumération LSA** mise à jour pour obtenir une énumération qui continue à partir du point où l’énumération précédente s’est arrêtée.


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




