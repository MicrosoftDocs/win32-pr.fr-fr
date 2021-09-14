---
title: Message MCIWNDM_NOTIFYSIZE (VFW. h)
description: Le \_ message MCIWNDM NOTIFYSIZE avertit la fenêtre parente d’une application que la taille de la fenêtre a changé.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- message MCIWNDM_NOTIFYSIZE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218660"
---
# <a name="mciwndm_notifysize-message"></a>\_Message MCIWNDM NOTIFYSIZE

Le message **MCIWNDM \_ NOTIFYSIZE** avertit la fenêtre parente d’une application que la taille de la fenêtre a changé.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle vers la fenêtre MCIWnd.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez activer la notification des modifications de la taille d’une fenêtre MCIWnd en spécifiant le \_ style de fenêtre NOTIFYSIZE MCIWNDF.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





