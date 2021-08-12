---
description: Récupère des informations sur l’espace utilisé par le cache Fichiers hors connexion.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667952"
---
# <a name="cscgetspaceusagew-function"></a>CSCGetSpaceUsageW fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Récupère des informations sur l’espace utilisé par le cache Fichiers hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lptzLocation* \[ in, out\]
</dt> <dd>

Emplacement du répertoire du cache.

</dd> <dt>

*dwSize nul* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *lptzLocation* , en caractères.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ in, out\]
</dt> <dd>

**Valeur DWORD** de poids fort du nombre maximal d’octets disponibles dans le cache.

</dd> <dt>

*lpdwMaxSpaceLow* \[ in, out\]
</dt> <dd>

**DWORD** de poids faible du nombre maximal d’octets disponibles dans le cache.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ in, out\]
</dt> <dd>

**Valeur DWORD** de poids fort du nombre actuel d’octets disponibles dans le cache.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ in, out\]
</dt> <dd>

**DWORD** de poids faible du nombre actuel d’octets disponibles dans le cache.

</dd> <dt>

*lpcntTotalFiles* \[ in, out\]
</dt> <dd>

Nombre total de fichiers dans le cache.

</dd> <dt>

*lpcntTotalDirs* \[ in, out\]
</dt> <dd>

Nombre total de répertoires dans le cache.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
