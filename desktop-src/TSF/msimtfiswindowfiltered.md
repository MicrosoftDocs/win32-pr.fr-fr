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
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105397"
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



 

## <a name="remarks"></a>Notes

Une fenêtre peut être filtrée par IActiveIMMApp :: FilterClientWindows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





