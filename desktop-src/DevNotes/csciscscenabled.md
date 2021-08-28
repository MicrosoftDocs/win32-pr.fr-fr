---
description: Détermine si Fichiers hors connexion est activé.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8678e48aedf6bda6cdb8beb5b78bb310a16d2829ebf6f3e5b0b8525c135aaf03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815459"
---
# <a name="csciscscenabled-function"></a>CSCIsCSCEnabled fonction)

\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]

Détermine si Fichiers hors connexion est activé.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si fichiers hors connexion est activé et **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSCQueryDatabaseStatus**](cscquerydatabasestatus.md)
</dt> </dl>

 

 
