---
description: Crée un certificat utilisateur à utiliser avec la Conférence NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543231"
---
# <a name="nmmakecert-function"></a>NmMakeCert fonction)

Crée un certificat utilisateur à utiliser avec la Conférence NetMeeting.

## <a name="syntax"></a>Syntaxe


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szFirstName* 
</dt> <dd>

Prénom de l’utilisateur.

</dd> <dt>

*szLastName* 
</dt> <dd>

Nom de famille de l’utilisateur.

</dd> <dt>

*szEmailName* 
</dt> <dd>

Nom de l’adresse de messagerie de l’utilisateur.

</dd> <dt>

*szCity* 
</dt> <dd>

ville de l'utilisateur.

</dd> <dt>

*szCountry* 
</dt> <dd>

Pays/région de l’utilisateur.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Valeur qui indique comment le certificat doit être créé. Les valeurs possibles sont les suivantes :



| Valeur                                                                                                                                                                                                                                                            | Signification                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <dt>**Nmmkcert \_ F \_ Cleanup \_ uniquement**</dt> <dt>0x00000004</dt> </dl>    | Supprimez l’ancien certificat sans en créer un nouveau. <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <dt>**Nmmkcert \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt> </dl>  | Supprimez l’ancien certificat créé précédemment avec cette fonction. <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <dt>**Nmmkcert \_ F \_ \_ ordinateur local**</dt> <dt>0x00000002</dt> </dl> | Créez le certificat dans le magasin de certificats de l’ordinateur local. <br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 1 si la fonction réussit et-1 si la fonction échoue.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Nmmkcert.dll</dt> </dl> |



 

 
