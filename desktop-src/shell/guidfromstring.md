---
description: Convertit une chaîne en GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Fonction GUIDFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864938"
---
# <a name="guidfromstring-function"></a>Fonction GUIDFromString

\[**GUIDFromString** est disponible via Windows XP avec Service Pack 2 (SP2) ou Windows Vista. Il peut être modifié ou non disponible dans les versions ultérieures. Les applications doivent utiliser [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) ou [**échec iidfromstring**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) à la place de cette fonction.\]

Convertit une chaîne en GUID.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PSZ* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers la chaîne se terminant par null à convertir. La chaîne doit se présenter sous la forme suivante :

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ à\]
</dt> <dd>

Type : **LPGUID**

Pointeur vers une mémoire tampon destinée à recevoir le GUID lorsque cette méthode est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

**True** si le GUID a été créé avec succès ; Sinon, **false**.

## <a name="remarks"></a>Notes

Cette fonction n’est pas déclarée dans un en-tête ou exportée par nom à partir d’un fichier. dll. Elle doit être chargée à partir de Shell32.dll en tant qu’ordinal 703 pour **GUIDFromStringA** et ordinal 704 pour **GUIDFromStringW**.

Elle est également accessible à partir de Shlwapi.dll en tant qu’ordinal 269 pour **GUIDFromStringA** et ordinal 270 pour **GUIDFromStringW**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **GUIDFromStringW** (Unicode) et **GUIDFromStringA** (ANSI)<br/>                |



 

 
