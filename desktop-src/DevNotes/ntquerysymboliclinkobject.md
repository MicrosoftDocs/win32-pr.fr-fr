---
description: Récupère la cible d’un lien symbolique.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543593"
---
# <a name="ntquerysymboliclinkobject-function"></a>NtQuerySymbolicLinkObject fonction)

\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]

Récupère la cible d’un lien symbolique.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LinkHandle* \[ dans\]
</dt> <dd>

Handle de l’objet de lien symbolique.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Pointeur vers une chaîne Unicode initialisée qui reçoit la cible du lien symbolique. Les membres **MaximumLength** et **buffer** doivent être définis si l’appel échoue.

</dd> <dt>

*ReturnedLength* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la longueur de la chaîne Unicode retournée dans le paramètre *LinkTarget* . Si la fonction retourne **une \_ mémoire tampon d’état \_ trop \_ petite**, cette variable reçoit la taille de mémoire tampon requise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne l’état **\_ Success** ou un état d’erreur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
