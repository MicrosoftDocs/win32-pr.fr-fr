---
title: SisCreateBackupStructure, fonction (sisbkup. h)
description: Crée une structure de sauvegarde SIS basée sur les informations fournies.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Sauvegarde de la fonction SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464782"
---
# <a name="siscreatebackupstructure-function"></a>SisCreateBackupStructure fonction)

La fonction **SisCreateBackupStructure** crée une structure de sauvegarde SIS basée sur les informations fournies.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*volumeRoot* \[ dans\]
</dt> <dd>

Nom de fichier de la racine du volume, sans la barre oblique inverse de fin, du volume à sauvegarder. Par exemple, spécifiez « C : » et non pas « C : \\ ».

</dd> <dt>

*sisBackupStructure* \[ à\]
</dt> <dd>

Structure de sauvegarde SIS retournée.

</dd> <dt>

*commonStoreRootPathname* \[ à\]
</dt> <dd>

Nom de chemin d’accès complet du magasin commun du volume spécifié. Par exemple, « c : \\ SIS Common Store ».

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ à\]
</dt> <dd>

Nombre de fichiers listés dans le paramètre *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ à\]
</dt> <dd>

Pointeur vers un tableau de noms de fichiers qui spécifie une liste de fichiers internes utilisés par SIS pour gérer le volume spécifié. Ces fichiers doivent être sauvegardés en même temps et de la même façon que les fichiers du magasin commun demandés par [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Notes

Cette fonction crée une structure de sauvegarde SIS, qui est utilisée par l’API de sauvegarde SIS pour créer et tenir à jour une liste des liens de fichiers sur le volume et les fichiers d’origine vers lesquels pointent les liens. Cette fonction ne doit être appelée qu’une seule fois pour chaque volume compatible SIS en cours de sauvegarde. Tous les fichiers du volume spécifié doivent être traités comme des fichiers de stockage commun et sauvegardés uniquement si SIS indique qu’ils le doivent.

Les paramètres *countOfCommonStoreFilesToBackUp* et *commonStoreFilesToBackUp* retournent ensemble une liste des fichiers qui doivent être sauvegardés, quels que soient les liens sauvegardés.

Si *countOfCommonStoreFilesToBackUp* a la valeur 0, *commonStoreFilesToBackUp* peut être un pointeur **null** . La valeur du paramètre *commonStoreFilesToBackUp* doit être ignorée.

Une fois l’opération de sauvegarde terminée, Désallouez la mémoire utilisée par le tableau de chaînes *commonStoreFilesToBackUp* en appelant [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

