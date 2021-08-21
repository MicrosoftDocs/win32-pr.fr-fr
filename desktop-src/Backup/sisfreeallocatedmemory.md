---
title: SisFreeAllocatedMemory, fonction (sisbkup. h)
description: Libère la mémoire allouée par les fonctions d’API SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Sauvegarde de la fonction SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702179"
---
# <a name="sisfreeallocatedmemory-function"></a>SisFreeAllocatedMemory fonction)

La fonction **SisFreeAllocatedMemory** libère de la mémoire allouée par les fonctions d’API SIS.

## <a name="syntax"></a>Syntaxe


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*allocatedSpace* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire allouée par l’API SIS.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Une fois l’appel à cette fonction terminé, l’appelant ne peut plus accéder à la mémoire libérée.

Cet appel doit être utilisé pour libérer la mémoire allouée pour les chaînes de paramètres *commonStoreRootPathname* retournées à partir de [**SisCreateBackupStructure**](siscreatebackupstructure.md) et [**SisCreateRestoreStructure**](siscreaterestorestructure.md), et le tableau de chaînes contenant des noms de fichiers de magasin commun retournés à partir de **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** et [**SisRestoredLink**](sisrestoredlink.md). Dans ce dernier cas, le tableau lui-même doit également être libéré en appelant **SisFreeAllocatedMemory**.

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

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





