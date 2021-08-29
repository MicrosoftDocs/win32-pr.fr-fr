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
ms.openlocfilehash: 6793aa6d0e0f3001a5c8c76b34ed6bbd1011ba17441fd709ee016d9d161a97b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525379"
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

## <a name="remarks"></a>Remarques

Vous pouvez activer la notification des modifications de la taille d’une fenêtre MCIWnd en spécifiant le \_ style de fenêtre NOTIFYSIZE MCIWNDF.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





