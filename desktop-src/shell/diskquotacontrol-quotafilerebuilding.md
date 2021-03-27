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
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972123"
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

## <a name="remarks"></a>Notes

Le fichier de quota est automatiquement régénéré lorsque les quotas sont activés sur le système ou lorsqu’une ou plusieurs entrées utilisateur sont marquées pour suppression.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




