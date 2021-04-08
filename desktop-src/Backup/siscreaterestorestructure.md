---
title: SisCreateRestoreStructure, fonction (sisbkup. h)
description: Crée une structure de restauration SIS basée sur les informations fournies.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Sauvegarde de la fonction SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843306"
---
# <a name="siscreaterestorestructure-function"></a>SisCreateRestoreStructure fonction)

La fonction **SisCreateRestoreStructure** crée une structure de restauration SIS basée sur les informations fournies.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*volumeRoot* \[ dans\]
</dt> <dd>

Nom de fichier de la racine du volume, sans la barre oblique inverse de fin, du volume à sauvegarder. Par exemple, spécifiez « C : » et non pas « C : \\ ». Le volume ne peut pas être le volume système ou de démarrage.

</dd> <dt>

*sisRestoreStructure* \[ à\]
</dt> <dd>

Structure de restauration SIS retournée. Cette structure doit être traitée comme opaque par l’appelant.

</dd> <dt>

*commonStoreRootPathname* \[ à\]
</dt> <dd>

Nom de chemin d’accès complet du magasin commun du volume spécifié. Par exemple, « c : \\ SIS Common Store ».

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ à\]
</dt> <dd>

Nombre de fichiers listés dans le paramètre *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ à\]
</dt> <dd>

Pointeur vers un tableau de noms de fichiers qui spécifie la liste des fichiers internes utilisés par SIS pour gérer le volume spécifié. Ces fichiers doivent être restaurés en même temps et de la même façon que les fichiers du magasin commun demandés par [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Notes

Cette fonction établit l’environnement de restauration sur le volume spécifié, de la façon dont [**SisCreateBackupStructure**](siscreatebackupstructure.md) établit l’environnement de sauvegarde sur le volume spécifié.

Notez que cette fonction n’identifie pas nécessairement le ou les fichiers du magasin commun qui correspondent à un ensemble de liens SIS sur le support de sauvegarde si ces fichiers ou fichiers du magasin commun existent toujours sur le disque. Le contenu du flux de données d’un fichier du magasin commun n’est jamais modifié une fois qu’il a été créé. par conséquent, si le fichier existe déjà sur le disque, il n’est pas nécessaire de le restaurer.

Les noms de fichiers Common-Store sont globalement uniques pour garantir l’intégrité de l’opération de restauration, même si elle ne se produit pas sur le même volume SIS que l’opération de sauvegarde a accédé.

Une fois l’opération de restauration terminée, libérez la mémoire utilisée par le tableau de chaînes *commonStoreFilesToRestore* en appelant [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

