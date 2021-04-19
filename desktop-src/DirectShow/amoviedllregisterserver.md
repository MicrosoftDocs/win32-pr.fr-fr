---
description: Obsolète. Utilisez AMovieDllRegisterServer2 à la place.
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: AMovieDllRegisterServer, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d93724c0f1ea6ed8b6cd2fa2b683a5ba9d45f0d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538133"
---
# <a name="amoviedllregisterserver-function"></a>AMovieDllRegisterServer fonction)

Obsolète. Utilisez [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) à la place.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DLLSETUP. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions de configuration des DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




