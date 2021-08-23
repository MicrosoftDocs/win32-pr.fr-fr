---
description: Initialise le partage IME.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 178b39c67d12473663eb93bc300651341a9c459c19680218fa2c6f7a939c688c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691379"
---
# <a name="finitimeshare-function"></a>FInitIMEShare fonction)

Initialise le partage IME.

## <a name="syntax"></a>Syntaxe


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Cette fonction doit être appelée avant d’appeler toute autre fonction de partage IME.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EndIMEShare**](endimeshare.md)
</dt> </dl>

 

 
