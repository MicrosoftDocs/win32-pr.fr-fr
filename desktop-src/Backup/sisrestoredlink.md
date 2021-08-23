---
title: SisRestoredLink, fonction (sisbkup. h)
description: Retourne les noms du ou des fichiers du magasin commun vers lesquels pointe le lien SIS restauré spécifié.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Sauvegarde de la fonction SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b330e4c6dfc5324f7041343865ea59885a0aedec01fa9c67014d3709a93834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021317"
---
# <a name="sisrestoredlink-function"></a>SisRestoredLink fonction)

La fonction **SisRestoredLink** retourne le nom du ou des fichiers du magasin commun vers lequel pointe le lien SIS restauré spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sisRestoreStructure* \[ dans\]
</dt> <dd>

Pointeur vers une structure de restauration SIS retournée à partir de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*restoredFileName* \[ dans\]
</dt> <dd>

Nom de fichier complet du fichier de liaison SIS restauré.

</dd> <dt>

*reparseData* \[ dans\]
</dt> <dd>

Pointeur vers le contenu du point d’analyse SIS. Ce point d’analyse contient des données décrivant le lien SIS restauré. Pour récupérer les données du point d’analyse d’un fichier, utilisez le code de contrôle [**FSCTL \_ obtenir le \_ \_ point d’analyse**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ dans\]
</dt> <dd>

Taille du contenu du point d’analyse SIS pointé par *reparseData*, en octets.

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ à\]
</dt> <dd>

Nombre de fichiers listés dans le paramètre *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ à\]
</dt> <dd>

Pointeur vers un tableau de noms de fichiers Common-Store. Ces fichiers doivent être restaurés en même temps et de la même façon que les fichiers du magasin commun demandés par [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

Si la valeur du paramètre *countOfCommonStoreFilesToRestore* n’est pas 0, la valeur du paramètre *commonStoreFilesToRestore* contient les noms des fichiers du magasin commun à restaurer suite à la restauration du lien SIS. Si la valeur est 0, cela signifie que les fichiers du magasin commun ont été retournés une fois ou qu’ils sont déjà présents sur le volume.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Remarques

Vous devez appeler cette fonction pour chaque lien SIS qui a été restauré.

Cette fonction renverra chaque fichier de magasin commun au plus une fois pour chaque opération de restauration. toute tentative de restauration de liens SIS supplémentaires qui affichent le même fichier de magasin commun n’entraîne pas le renvoi du nom de fichier du magasin commun.

Cette fonction ne retourne pas de fichier de magasin commun qui n’a pas également été retourné dans un appel à [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) pendant l’opération de sauvegarde, en supposant que les données de réanalyse SIS stockées sur le média n’ont pas été endommagées.

Lors de la restauration d’un lien SIS, votre opération de restauration doit créer uniquement le fichier partiellement alloué approprié, initialiser toutes les plages allouées, puis écrire les données de nouvelle analyse SIS exactement telles qu’elles ont été lues pendant l’opération de sauvegarde. Il est essentiel que votre opération de restauration crée des fichiers partiellement alloués avec des plages non allouées, plutôt que des fichiers partiellement alloués (ou des fichiers non distants) initialisés avec des zéros.

Notez que cette fonction n’identifie pas nécessairement le ou les fichiers du magasin commun qui correspondent à un ensemble de liens SIS sur le support de sauvegarde si ces fichiers ou fichiers du magasin commun existent toujours sur le disque. Le contenu du flux de données d’un fichier du magasin commun n’est jamais modifié une fois qu’il a été créé. par conséquent, si le fichier existe déjà sur le disque, il n’est pas nécessaire de le restaurer.

Les noms de fichiers Common-Store sont globalement uniques pour garantir l’intégrité de l’opération de restauration, même si elle ne se produit pas sur le même volume SIS que l’opération de sauvegarde a accédé.

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
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

