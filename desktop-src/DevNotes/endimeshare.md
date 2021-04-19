---
description: Met fin au partage IME.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523025"
---
# <a name="endimeshare-function"></a>EndIMEShare fonction)

Met fin au partage IME.

## <a name="syntax"></a>Syntaxe


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Cette fonction doit être appelée après l’appel de la dernière fonction de partage IME.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FInitIMEShare**](finitimeshare.md)
</dt> </dl>

 

 
