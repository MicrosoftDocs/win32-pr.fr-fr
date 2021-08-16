---
title: SisFreeRestoreStructure, fonction (sisbkup. h)
description: Libère la mémoire allouée pour la structure de restauration SIS spécifiée et effectue des tâches qui préparent le filtre SIS à configurer correctement les liens créés lors de l’opération de restauration.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Sauvegarde de la fonction SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a787283f933ae4ccd2d8100c39e6118b40c545c030bb236a27a2f1598417742e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835547"
---
# <a name="sisfreerestorestructure-function"></a>SisFreeRestoreStructure fonction)

La fonction **SisFreeRestoreStructure** libère la mémoire allouée pour la structure de restauration SIS spécifiée et effectue des tâches qui préparent le filtre sis à configurer correctement les liens créés lors de l’opération de restauration.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sisRestoreStructure* \[ dans\]
</dt> <dd>

Pointeur vers une structure de restauration SIS retournée à partir de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Remarques

L’accès aux liens SIS avant l’exécution de l’appel à cette fonction peut entraîner une vérification du volume ou une lecture partielle du contenu du lien.

Notez qu’il n’est pas possible de supposer que cela libère uniquement de la mémoire. Par exemple, cette fonction peut également effectuer des opérations administratives supplémentaires pour l’architecture SIS. Par conséquent, appelez cette fonction même si votre opération de restauration se termine immédiatement après.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

