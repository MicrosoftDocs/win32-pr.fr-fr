---
title: Message MCIWNDM_NOTIFYERROR (VFW. h)
description: Le \_ message MCIWNDM NOTIFYERROR notifie la fenêtre parente d’une application qu’une erreur MCI s’est produite.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- message MCIWNDM_NOTIFYERROR Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dcca10f593c14e1532aa53b59b8c0bb106ea721ad0d09bde742727fddaeb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374130"
---
# <a name="mciwndm_notifyerror-message"></a>\_Message MCIWNDM NOTIFYERROR

Le message **MCIWNDM \_ NOTIFYERROR** notifie la fenêtre parente d’une application qu’une erreur MCI s’est produite.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle vers la fenêtre MCIWnd.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*
</dt> <dd>

Code numérique de l’erreur MCI.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez activer la notification d’erreur MCI en spécifiant le \_ style de fenêtre MCIWNDF NOTIFYERROR.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





