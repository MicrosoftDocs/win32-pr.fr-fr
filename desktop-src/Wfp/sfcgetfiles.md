---
description: Répertorie les fichiers protégés.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: SfcGetFiles, fonction (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 3201621808708229419542acd7fa0caab0aa7f6e7d38bfe723b7f53bc68c4005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999279"
---
# <a name="sfcgetfiles-function"></a>SfcGetFiles fonction)

\[Cette fonction peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. la prise en charge de cette fonction a été supprimée dans Windows Vista et Windows Server 2008. Utilisez à la place les fonctions prises en charge listées dans [fonctions WRP](wfp-functions.md) .\]

Répertorie les fichiers protégés.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProtFileData* \[ à\]
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ entrée de fichier PPROTECT**](pprotect-file-entry.md) qui contient la liste des fichiers protégés.

</dd> <dt>

*FileCount* \[ à\]
</dt> <dd>

Pointeur vers un emplacement contenant une valeur ULONG qui correspond au nombre de fichiers protégés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est STATUs \_ successful. Si la fonction échoue, elle retourne le code d’erreur NTSTATUS approprié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_entrée de fichier PPROTECT \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




