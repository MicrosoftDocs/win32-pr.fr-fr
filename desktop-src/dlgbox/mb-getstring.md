---
title: MB_GetString fonction (User. h)
description: Retourne des chaînes pour les boutons de boîte de message standard.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Boîtes de dialogue de MB_GetString fonction
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd984a2f65ab8c2eed8a77fffa56af1d94633c828196428a674c9eee78c3ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985359"
---
# <a name="mb_getstring-function"></a>\_Fonction GetString de MB

Retourne des chaînes pour les boutons de boîte de message standard.

## <a name="syntax"></a>Syntaxe


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wBtn* 
</dt> <dd>

ID de la chaîne à retourner. Celles-ci sont identifiées par les valeurs d’ID de commande de la boîte de dialogue répertoriées dans winuser. h.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne, ou NULL si introuvable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>User. h</dt> </dl>     |
| Bibliothèque<br/> | <dl> <dt>User32. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





