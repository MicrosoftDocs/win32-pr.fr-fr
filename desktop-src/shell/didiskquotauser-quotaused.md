---
description: Obtient l’utilisation actuelle du disque de l’utilisateur, en octets.
title: DIDiskQuotaUser. QuotaUsed, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: c1584f2abd7fbb6d11d345ec78499b08dc0337e0ddd6bd6300e42a4ec3c2acec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459930"
---
# <a name="didiskquotauserquotaused-property"></a>DIDiskQuotaUser. QuotaUsed, propriété

Obtient l’utilisation actuelle du disque de l’utilisateur, en octets.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Valeur de la propriété

Valeur **entière** définie sur la quantité d’espace disque actuellement utilisée. Si la compression de fichiers NTFS est activée, **QuotaUsed** reflète la quantité d’espace disque requise par les données dans un État non compressé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**QuotaUsedText**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




