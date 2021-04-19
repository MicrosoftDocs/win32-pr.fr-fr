---
description: Gère le \_ message WM CTLCOLOR pour les applications qui utilisent CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544108"
---
# <a name="ctl3dctlcolorex-function"></a>Ctl3dCtlColorEx fonction)

Gère le message **WM \_ CTLCOLOR** pour les applications qui utilisent CTL3D.

## <a name="syntax"></a>Syntaxe


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wm* 
</dt> <dd>

Message **WM \_ CTLCOLOR** pour l’application.

</dd> <dt>

*wParam* 
</dt> <dd>

Handle vers le contexte d’affichage (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Handle d’une fenêtre enfant (contrôle).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un handle au pinceau approprié si la fonction est réussie ; dans le cas contraire, elle retourne `(HBRUSH)(0)` indiquant qu’une erreur s’est produite.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
