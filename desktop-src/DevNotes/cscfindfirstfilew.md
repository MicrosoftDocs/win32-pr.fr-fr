---
description: Recherche un fichier dans le cache de Fichiers hors connexion qui répond aux critères spécifiés.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527329"
---
# <a name="cscfindfirstfilew-function"></a>CSCFindFirstFileW fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Recherche un fichier dans le cache de Fichiers hors connexion qui répond aux critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszFileName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie un répertoire UNC ou un chemin d’accès valide.

</dd> <dt>

*lpFind32* \[ à\]
</dt> <dd>

Pointeur vers la structure [**de \_ \_ données de recherche Win32**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) qui reçoit des informations sur le fichier ou le sous-répertoire.

</dd> <dt>

*lpdwStatus* \[ à\]
</dt> <dd>

Code NTSTATUS qui indique l’état de l’appel.

</dd> <dt>

*lpdwPinCount* \[ à\]
</dt> <dd>

Ce paramètre est différent de zéro si le fichier a été rendu disponible hors connexion ou 0 dans le cas contraire.

</dd> <dt>

*lpdwHintFlags* \[ à\]
</dt> <dd>

Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                | Signification                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <dt>**Indicateur \_ \_ \_ Code confidentiel \_ d’indicateur CSC utilisateur**</dt> <dt>0x01</dt> </dl>                                | Un utilisateur a rendu le fichier disponible hors connexion.<br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <dt>**Indicateur \_ \_Code pin d’indicateur CSC \_ \_ inherit \_ User**</dt> <dt>0x02</dt> </dl>       | Un utilisateur a rendu le parent disponible hors connexion et marqué le parent de sorte que ses enfants soient disponibles hors connexion.<br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <dt>**Indicateur \_ \_Code PIN de l’indicateur CSC \_ \_ inherit \_ System**</dt> <dt>0x04</dt> </dl> | Un administrateur ou une stratégie de groupe a rendu le parent disponible hors connexion et marqué le parent de telle sorte que ses enfants soient disponibles hors connexion.<br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <dt>**Indicateur \_ \_Système de \_ pin \_ d’indicateur CSC**</dt> <dt>0x10</dt> </dl>                          | Un administrateur ou une stratégie de groupe a rendu le fichier disponible hors connexion.<br/>                                                                      |



 

</dd> <dt>

*lpOrgFileTime* \[ à\]
</dt> <dd>

Pointeur vers une structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) pour recevoir les informations de date et d’heure du fichier ou du sous-répertoire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est un handle de recherche utilisé dans un appel ultérieur à [**CSCFindNextFileW**](cscfindnextfilew.md) ou [**CSCFindClose**](cscfindclose.md).

Si la fonction échoue, la valeur de retour est **INVALID\_HANDLE\_VALUE**.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
