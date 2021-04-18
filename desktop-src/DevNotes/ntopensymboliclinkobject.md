---
description: Ouvre un lien symbolique existant.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526731"
---
# <a name="ntopensymboliclinkobject-function"></a>NtOpenSymbolicLinkObject fonction)

\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]

Ouvre un lien symbolique existant.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LinkHandle* \[ à\]
</dt> <dd>

Handle vers l’objet de lien symbolique récemment ouvert.

</dd> <dt>

*DesiredAccess* \[ dans\]
</dt> <dd>

[**\_ Masque d’accès**](../secauthz/access-mask.md) qui spécifie l’accès demandé à l’objet d’annuaire. Il est courant d’utiliser \_ la lecture générique pour que le handle puisse être passé à la fonction [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .

</dd> <dt>

*ObjectAttributes* \[ dans\]
</dt> <dd>

Attributs de l’objet d’annuaire. Pour initialiser la structure des **\_ attributs d’objet** , utilisez la macro **InitializeObjectAttributes** . Si l’appelant n’est pas exécuté dans un contexte de thread système, il doit spécifier l’indicateur de **\_ \_ handle de noyau obj** lors de l’initialisation de la structure. Pour plus d’informations, consultez la documentation de ces éléments dans la documentation du kit WDK.

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

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
