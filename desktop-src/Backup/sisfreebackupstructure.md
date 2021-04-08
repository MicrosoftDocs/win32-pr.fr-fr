---
title: SisFreeBackupStructure, fonction (sisbkup. h)
description: Libère la structure de sauvegarde SIS spécifiée.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Sauvegarde de la fonction SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740693"
---
# <a name="sisfreebackupstructure-function"></a>SisFreeBackupStructure fonction)

La fonction **SisFreeBackupStructure** libère la structure de sauvegarde SIS spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sisBackupStructure* \[ dans\]
</dt> <dd>

Pointeur vers la structure de sauvegarde SIS retournée par [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Notes

Cette fonction doit être appelée une fois que l’opération de sauvegarde est terminée pour le volume identifié par la valeur du paramètre *sisBackupStructure* .

Notez qu’il n’est pas possible de supposer que cela libère uniquement de la mémoire. Par exemple, cette fonction peut également effectuer des opérations administratives supplémentaires pour l’architecture SIS. Par conséquent, appelez cette fonction même si votre opération de sauvegarde se termine immédiatement après.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

