---
description: Commence la surveillance de l’inactivité.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539943"
---
# <a name="beginidledetection-function"></a>BeginIdleDetection fonction)

\[Cette fonction n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Utilisez plutôt la fonction **GetLastInputInfo** .\]

Commence la surveillance de l’inactivité.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfnCallback* 
</dt> <dd>

Fonction appelée lorsque l’état inactif change. Ce rappel est défini comme suit :

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwIdleMin* 
</dt> <dd>

Nombre de minutes d’inactivité avant l’appel à la fonction de rappel.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Ce paramètre doit avoir la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 si la fonction est réussie ; Sinon, elle retourne un code d’erreur. Par exemple, si *dwReserved* est autre chose que 0, **les \_ \_ données non valides** de l’erreur sont retournées.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Cette fonction n’est pas exportée par nom ; Spécifiez l’ordinal 3 lors de l’appel de **GetProcAddress**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
