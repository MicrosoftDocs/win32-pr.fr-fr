---
title: SisCSFilesToBackupForLink, fonction (sisbkup. h)
description: Retourne des informations décrivant les fichiers du magasin commun vers lesquels pointe le lien SIS spécifié.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Sauvegarde de la fonction SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e39d4370e68b67a5c05c1f259c52190be3b931dd02164da191bacf879cd6cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835557"
---
# <a name="siscsfilestobackupforlink-function"></a>SisCSFilesToBackupForLink fonction)

La fonction **SisCSFilesToBackupForLink** retourne des informations décrivant les fichiers de magasin commun vers lesquels pointe le lien SIS spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sisBackupStructure* \[ dans\]
</dt> <dd>

Pointeur vers la structure de sauvegarde SIS retournée par [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> <dt>

*reparseData* \[ dans\]
</dt> <dd>

Pointeur vers le contenu du point d’analyse SIS. Ce point d’analyse contient des données décrivant un lien SIS. Pour récupérer les données du point d’analyse d’un fichier, utilisez le code de contrôle [**FSCTL \_ obtenir le \_ \_ point d’analyse**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ dans\]
</dt> <dd>

Taille du contenu du point d’analyse SIS pointé par *reparseData*, en octets.

</dd> <dt>

*thisFileContext* \[ à\]
</dt> <dd>

Pointeur vers une chaîne de contexte fournie par l’application de sauvegarde appelant cette fonction. Le contenu de cette chaîne de contenu est entièrement déterminé par cette application de sauvegarde et n’est pas interprété par l’API de sauvegarde SIS. Ce paramètre est facultatif. s’il n’est pas utilisé, affectez la valeur **null** à ce paramètre. La valeur de ce paramètre ne sera pas traitée dans ce cas.

</dd> <dt>

*matchingFileContext* \[ à\]
</dt> <dd>

Pointeur doublement indirect vers la chaîne de contexte du lien SIS identifié par les informations passées dans les quatre premiers paramètres de cette fonction. Ce paramètre est facultatif. Si une chaîne de contexte n’est pas fournie comme valeur du paramètre *thisFileContext* , affectez la valeur **null** à ce paramètre. La valeur de ce paramètre ne sera pas traitée dans ce cas.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ à\]
</dt> <dd>

Nombre de fichiers listés dans le paramètre *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ à\]
</dt> <dd>

Pointeur vers un tableau de noms de fichiers. Ces fichiers doivent être sauvegardés en même temps et de la même façon que les fichiers du magasin commun demandés par [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire. Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.

## <a name="remarks"></a>Remarques

L’application de sauvegarde ne doit appeler cette fonction qu’une seule fois pour chaque fichier de liaison SIS en cours de sauvegarde.

L’application de sauvegarde peut identifier un point d’analyse SIS par sa balise, la balise d’analyse d’e/s de \_ \_ balise \_ SIS. Cette balise est définie dans Winnt. h.

Si ce point d’analyse identifié par la valeur du paramètre *reparseData* décrit la première instance d’un fichier à sauvegarder, cette fonction retourne **null** comme valeur du paramètre *matchingFileContext* et initialise la valeur du tableau *commonStoreFilesToBackUp* de chaînes avec les noms du ou des fichiers du magasin commun qui doivent être sauvegardés (e). Dans le cas contraire, cette fonction définit la valeur du paramètre *matchingFileContext* sur la chaîne de contexte correspondant à la première instance du fichier spécifié et affecte à la valeur du paramètre *countOfCommonStoreFilesToBackUp* la valeur 0. S’il existe plusieurs fichiers de magasin commun correspondant au lien spécifié, la valeur du paramètre *thisFileContext* est la chaîne de contexte correspondant au premier fichier de magasin commun retourné dans le tableau qui est, commonStoreFilesToBackUp \[ 0 \] .

La version actuelle de cette fonction retournera au plus un fichier de magasin commun, mais il est possible que dans les versions ultérieures, un seul lien puisse être sauvegardé par plusieurs fichiers du magasin commun, par exemple, un pour chaque flux du fichier afin que votre application de sauvegarde prenne en charge plusieurs fichiers dans chaque appel à cette fonction. Dans tous les cas, chaque fichier de magasin commun est retourné au plus une fois pour chaque passe de sauvegarde.

Votre application de sauvegarde doit sauvegarder ou restaurer le ou les fichiers du magasin commun identifiés par le nom de fichier ou les noms de fichiers retournés dans le paramètre *commonStoreFilesToBackUp* . Qu’il y ait ou non un fichier de magasin commun, votre application de sauvegarde doit sauvegarder le fichier de liaison SIS tel qu’il existe sur le disque, par exemple, comme un point d’analyse et un fichier partiellement alloué, et probablement sans aucune plage remplie. Votre application de sauvegarde peut sauvegarder ou restaurer le ou les fichiers du magasin commun immédiatement, les différer ou les combiner en fonction des besoins.

Une fois l’opération de sauvegarde terminée, Désallouez la mémoire utilisée par le tableau de chaînes *commonStoreFilesToBackUp* en appelant [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

