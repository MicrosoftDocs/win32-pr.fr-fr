---
description: Définit ou obtient le seuil de quota par défaut.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: DiskQuotaControl. DefaultQuotaThreshold, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971970"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>DiskQuotaControl. DefaultQuotaThreshold, propriété

Définit ou obtient le seuil de quota par défaut.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Valeur de la propriété

Valeur **entière** qui est définie sur le seuil d’avertissement par défaut pour les nouveaux utilisateurs, en octets.

## <a name="remarks"></a>Notes

Le seuil de quota par défaut est appliqué automatiquement aux nouveaux utilisateurs du volume. Si l’utilisation du disque d’un utilisateur dépasse cette valeur et que la propriété [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) est définie sur **true**, le système génère une entrée de journal des événements. Par exemple, si le seuil par défaut est de 10,0 Mo, la valeur de la propriété est « 10,0 Mo ». Si le volume n’a pas de seuil par défaut, la propriété a la valeur « aucune limite » ou l’équivalent localisé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




