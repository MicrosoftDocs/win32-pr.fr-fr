---
description: Fonction AMovieDllUnregisterServer-obsolète. Utilisez AMovieDllRegisterServer2 à la place.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: AMovieDllUnregisterServer, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099927"
---
# <a name="amoviedllunregisterserver-function"></a>AMovieDllUnregisterServer fonction)

Obsolète. Utilisez [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) à la place.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AMovieDllUnregisterServer(void);
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

 

 




