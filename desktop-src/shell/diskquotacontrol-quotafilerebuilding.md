---
description: Obtient une valeur booléenne qui indique si le fichier de quota du volume est en cours de reconstruction.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: DiskQuotaControl. QuotaFileRebuilding, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8e90d5d920392b9b518fed619aeb4f8c7b99d830fad9f6f901c59fe6128ca94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710519"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>DiskQuotaControl. QuotaFileRebuilding, propriété

Obtient une valeur booléenne qui indique si le fichier de quota du volume est en cours de reconstruction.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété a la valeur **true** si le fichier de quota est en cours de reconstruction, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Le fichier de quota est automatiquement régénéré lorsque les quotas sont activés sur le système ou lorsqu’une ou plusieurs entrées utilisateur sont marquées pour suppression.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




