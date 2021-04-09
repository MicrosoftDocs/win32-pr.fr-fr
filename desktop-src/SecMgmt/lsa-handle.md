---
description: Handle de l’objet de stratégie locale.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034567"
---
# <a name="lsa_handle"></a>\_handle LSA

Le type de données du **\_ handle LSA** est un descripteur de l’objet de [**stratégie**](policy-object.md) locale.


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a>Notes

Avant de pouvoir utiliser l’API de stratégie locale, votre application doit ouvrir un handle vers un objet de [**stratégie**](policy-object.md) . Pour ce faire, appelez [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy). Cette fonction retourne un handle que votre application peut ensuite spécifier dans les appels de fonction de stratégie LSA suivants.

Chaque handle possède un ensemble d’autorisations associées qui déterminent les opérations que votre application peut effectuer sur l’objet de [**stratégie**](policy-object.md) à l’aide du descripteur. Votre application peut ouvrir plusieurs descripteurs à la fois sur l’objet de **stratégie** . Lorsqu’un descripteur n’est plus nécessaire, votre application doit la fermer en appelant [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

