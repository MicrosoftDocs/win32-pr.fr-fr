---
title: Message MCIWNDM_NOTIFYPOS (VFW. h)
description: Le \_ message MCIWNDM NOTIFYPOS notifie la fenêtre parente d’une application que la position de la fenêtre a changé.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- message MCIWNDM_NOTIFYPOS Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218665"
---
# <a name="mciwndm_notifypos-message"></a>\_Message MCIWNDM NOTIFYPOS

Le message **MCIWNDM \_ NOTIFYPOS** notifie la fenêtre parente d’une application que la position de la fenêtre a changé.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle vers la fenêtre MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*imprim*
</dt> <dd>

Décrit la nouvelle position.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez activer la notification des modifications apportées à la position d’une fenêtre MCIWnd en spécifiant le \_ style de fenêtre NOTIFYPOS MCIWNDF.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





