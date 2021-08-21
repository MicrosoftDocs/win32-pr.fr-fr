---
title: SisRestoredCommonStoreFile, fonction (sisbkup. h)
description: Signale à l’architecture SIS qu’un fichier de magasin commun a été écrit.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Sauvegarde de la fonction SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 389d40b76614fe64038133c8cc0623706d4f2be82e68b3e096b59b3023f08bf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529489"
---
# <a name="sisrestoredcommonstorefile-function"></a>SisRestoredCommonStoreFile fonction)

La fonction **SisRestoredCommonStoreFile** signale à l’architecture SIS qu’un fichier de magasin commun a été écrit.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sisRestoreStructure* \[ dans\]
</dt> <dd>

Pointeur vers une structure de restauration SIS retournée à partir de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*commonStoreFileName* \[ dans\]
</dt> <dd>

Nom du fichier de stockage commun restauré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Remarques

Cette fonction doit être appelée une fois que vous avez restauré un fichier de magasin commun. Il informe l’architecture SIS qu’un nouveau fichier de magasin commun a été écrit, afin que l’architecture SIS puisse effectuer des tâches de maintenance internes, telles que l’initialisation de ses structures de données internes ou la résolution des liens vers le fichier de magasin commun.

Votre opération de restauration doit restaurer uniquement les fichiers du magasin commun signalés par [**SisRestoredLink**](sisrestoredlink.md), même s’il existe des fichiers de stockage commun supplémentaires sur le support de sauvegarde. Votre opération de restauration peut restaurer les liens SIS et les fichiers du magasin commun dans l’ordre de leur choix. Toutefois, il doit appeler **SisRestoredLink** après la restauration d’un lien, et il doit appeler cette fonction après la restauration d’un fichier de magasin commun. Étant donné que l’opération de restauration ne peut pas identifier les fichiers de magasin commun qui seront restaurés tant que les noms de fichiers ne sont pas signalés par la restauration d’un lien, votre opération de restauration restaurera toujours un fichier de magasin commun après qu’au moins un lien faisant référence à lui soit restauré. Toutefois, vous pouvez ensuite restaurer des liens SIS supplémentaires qui pointent vers ce fichier de magasin commun.

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

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

