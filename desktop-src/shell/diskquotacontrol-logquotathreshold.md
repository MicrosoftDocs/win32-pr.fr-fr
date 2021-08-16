---
description: Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse son seuil de quota attribué.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: DiskQuotaControl. LogQuotaThreshold, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bb2a2073a791fcbb8e5bb6db83480f0fcea52b35e0380c20be730265d5bb34ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090639"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>DiskQuotaControl. LogQuotaThreshold, propriété

Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse son seuil de quota attribué.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété a la valeur **true** si une entrée du journal des événements système est effectuée lorsque l’utilisateur dépasse son seuil d’avertissement de quota, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




