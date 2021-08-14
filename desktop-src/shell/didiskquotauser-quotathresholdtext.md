---
description: Obtient le seuil d’avertissement de l’utilisateur sous la forme d’une chaîne de texte.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: DIDiskQuotaUser. QuotaThresholdText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ca2136936d45850726e64b61c4fae62889d2b5e5ea30cd2b9c3a98357006e962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224674"
---
# <a name="didiskquotauserquotathresholdtext-property"></a>DIDiskQuotaUser. QuotaThresholdText, propriété

Obtient le seuil d’avertissement de l’utilisateur sous la forme d’une chaîne de texte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de chaîne qui contient le seuil d’avertissement de l’utilisateur. Si l’utilisation du disque d’un utilisateur dépasse cette valeur et que la propriété [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) est définie sur **true**, le système génère une entrée de journal des événements.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet IDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




