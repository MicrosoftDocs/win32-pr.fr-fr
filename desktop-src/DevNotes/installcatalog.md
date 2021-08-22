---
description: Installe un catalogue dans un répertoire.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 240754024135b5bd5aa48529d49080afbdb04e170987102346cdda2c59b12427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955928"
---
# <a name="installcatalog-function"></a>InstallCatalog fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Installe un catalogue dans un répertoire.

## <a name="syntax"></a>Syntaxe


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CatalogFullPath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui représente le chemin d’accès complet du catalogue avant l’installation.

</dd> <dt>

*NewBaseName* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers le nouveau nom de base.

</dd> <dt>

*NewCatalogFullPath* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une chaîne qui représente le chemin d’accès complet du catalogue après l’installation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction n’étant pas implémentée actuellement, elle ne retourne pas de valeur réelle.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
