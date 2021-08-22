---
title: MsimtfIsWindowFiltered fonction)
description: La fonction MsimtfIsWindowFiltered teste si la fenêtre donnée est filtrée par AIMM (gestionnaire de méthode d’entrée actif).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered fonction Text Services Framework
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f3841ed5c0436d991d02291c1e395f42d6b31b66f442a3caac0b2062fc27db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476749"
---
# <a name="msimtfiswindowfiltered-function"></a>MsimtfIsWindowFiltered fonction)

La fonction **MsimtfIsWindowFiltered** teste si la fenêtre donnée est filtrée par AIMM (gestionnaire de méthode d’entrée actif).

## <a name="syntax"></a>Syntaxe


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de fenêtre à tester.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée



| Code de retour                                                                          | Description                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**:**</dt> </dl>  | Si cette fenêtre est filtrée par le gestionnaire de méthode d’entrée actif.<br/>     |
| <dl> <dt>**FAUSSES**</dt> </dl> | Si cette fenêtre n’est pas filtrée par le gestionnaire de méthode d’entrée actif.<br/> |



 

## <a name="remarks"></a>Remarques

Une fenêtre peut être filtrée par IActiveIMMApp :: FilterClientWindows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





