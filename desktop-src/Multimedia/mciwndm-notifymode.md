---
title: Message MCIWNDM_NOTIFYMODE (VFW. h)
description: Le \_ message MCIWNDM NOTIFYMODE notifie la fenêtre parente d’une application que le mode d’opération du périphérique MCI a changé.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- message MCIWNDM_NOTIFYMODE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364295"
---
# <a name="mciwndm_notifymode-message"></a>\_Message MCIWNDM NOTIFYMODE

Le message **MCIWNDM \_ NOTIFYMODE** notifie la fenêtre parente d’une application que le mode d’opération du périphérique MCI a changé.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle vers la fenêtre MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*mode*
</dt> <dd>

Entier correspondant au mode MCI.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez activer la notification des modifications de mode d’un appareil MCI en spécifiant le \_ style de fenêtre MCIWNDF NOTIFYMODE.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





