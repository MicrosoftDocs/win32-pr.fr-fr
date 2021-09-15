---
description: Crée un profil utilisateur pour un utilisateur spécifié.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412562"
---
# <a name="createuserprofileex-function"></a>CreateUserProfileEx fonction)

\[cette fonction n’est pas disponible à partir de Windows Vista.\]

Crée un profil utilisateur pour un utilisateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSid* \[ dans\]
</dt> <dd>

Type : **PSID**

SID du nouvel utilisateur.

</dd> <dt>

*lpUserName* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers une mémoire tampon qui contient le nom d’utilisateur du nouvel utilisateur.

</dd> <dt>

*lpUserHive* \[ dans, facultatif\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers une mémoire tampon qui contient la [ruche de Registre](../sysinfo/registry-hives.md) à utiliser. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpProfileDir* \[ out, facultatif\]
</dt> <dd>

Type : **LPTStr**

Pointeur vers une mémoire tampon qui, lorsque cette fonction est retournée, reçoit le chemin d’accès au répertoire de profil de l’utilisateur. Ce paramètre peut être **NULL**.

</dd> <dt>

*dwDirSize* \[ dans\]
</dt> <dd>

Type : **DWORD**

Taille de la mémoire tampon spécifiée par *lpProfileDir*, dans TCHARs.

</dd> <dt>

*bWin9xUpg* \[ dans\]
</dt> <dd>

Type : **bool**

**TRUE** si le profil utilisateur est créé dans le cadre d’une migration de profil à partir de Windows 9x ; Sinon, **false**.

si la **valeur est TRUE**, le profil utilisateur est configuré dans le répertoire de profil par défaut, normalement C : \\ Documents et Paramètres \\ *nom d’utilisateur*. Si ce répertoire existe déjà, il est utilisé. Si ce n’est pas le cas, il est créé.

Si la **valeur est false**, le répertoire de profil par défaut est créé s’il n’existe pas. Si le répertoire de profil par défaut existe déjà, un nouveau répertoire est créé pour ce profil utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **bool**

Retourne la **valeur true** si le nouveau profil utilisateur a été créé avec succès ; Sinon, **false**.

## <a name="remarks"></a>Notes

Cette fonction n’est pas déclarée dans les en-têtes du kit de développement logiciel (SDK) et n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison à Userenv.dll. La version ANSI de la fonction, **CreateUserProfileExA** est référencée à partir de Userenv.dll en tant qu’ordinal 153. La version Unicode, **CreateUserProfileExW** est référencée sous la forme ordinale 154.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/>  | Windows XP<br/>                                                                  |
| DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Noms Unicode et ANSI<br/> | **CreateUserProfileExW** (Unicode) et **CreateUserProfileExA** (ANSI)<br/>      |



 

 
