---
description: Obtient le seuil de quota par défaut sous la forme d’une chaîne de texte.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: DiskQuotaControl. DefaultQuotaThresholdText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112323"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>DiskQuotaControl. DefaultQuotaThresholdText, propriété

Obtient le seuil de quota par défaut sous la forme d’une chaîne de texte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de chaîne qui contient le seuil de quota par défaut pour le volume.

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

 

 




