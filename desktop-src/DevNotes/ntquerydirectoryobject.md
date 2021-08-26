---
description: Récupère des informations sur l’objet d’annuaire spécifié.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 11c7240cf63fa2f7e13338a0e0459e172e41aa1ed71db90c661b8aad0915d670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079669"
---
# <a name="ntquerydirectoryobject-function"></a>NtQueryDirectoryObject fonction)

\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]

Récupère des informations sur l’objet d’annuaire spécifié.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DirectoryHandle* \[ dans\]
</dt> <dd>

Handle de l’objet d’annuaire.

</dd> <dt>

*Mémoire tampon* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les informations d’annuaire. Cette mémoire tampon reçoit une ou plusieurs structures d' **\_ \_ informations d’annuaire d’objets** , la dernière ayant la **valeur null**, suivie de chaînes qui contiennent les noms des entrées de répertoire. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*Longueur* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon de sortie fournie par l’utilisateur, en octets.

</dd> <dt>

*ReturnSingleEntry* \[ dans\]
</dt> <dd>

Indique si la fonction doit retourner une seule entrée.

</dd> <dt>

*RestartScan* \[ dans\]
</dt> <dd>

Indique s’il faut redémarrer l’analyse ou continuer l’énumération à l’aide des informations passées dans le paramètre de *contexte* .

</dd> <dt>

*Contexte* \[ in, out\]
</dt> <dd>

Contexte d’énumération.

</dd> <dt>

*ReturnLength* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la longueur des informations de répertoire retournées dans la mémoire tampon de sortie, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne l’état **\_ Success** ou un état d’erreur.

## <a name="remarks"></a>Remarques

Voici la définition de la structure d' **\_ \_ informations de répertoire** de l’objet.

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
