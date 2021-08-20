---
description: Vérifie un fichier catalogue unique.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: eb4012a04b4da9e353a5d771f9b9e61d4bfba8b45ed6a7d5c65a81c197ff9be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075743"
---
# <a name="verifycatalogfile-function"></a>VerifyCatalogFile fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Vérifie un fichier catalogue unique.

## <a name="syntax"></a>Syntaxe


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CatalogFullPath* 
</dt> <dd>

Chemin d’accès qualifié complet du fichier catalogue à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne l' **erreur \_ réussite**; sinon, elle retourne l’erreur de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

Si le catalogue est un catalogue signé par Authenticode, cette fonction retourne **l' \_ erreur \_ \_ éditeur approuvé Authenticode** si elle est réussie ; sinon, elle retourne une **erreur \_ Authenticode \_ Trust \_ non \_ établi**.

Si la fonction ne peut pas déterminer si le serveur de publication est approuvé, elle peut également retourner une erreur non **\_ identifiée \_**.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
