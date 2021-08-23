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
ms.openlocfilehash: 46fe35fd507f20e41e0a9b563ded5c9cf46e9c557893bc9287d65cbdf651b24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691639"
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

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
