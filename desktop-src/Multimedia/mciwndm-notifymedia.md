---
title: Message MCIWNDM_NOTIFYMEDIA (VFW. h)
description: Le \_ message MCIWNDM NOTIFYMEDIA notifie la fenêtre parente d’une application que le média a changé.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- message MCIWNDM_NOTIFYMEDIA Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364292"
---
# <a name="mciwndm_notifymedia-message"></a>\_Message MCIWNDM NOTIFYMEDIA

Le message **MCIWNDM \_ NOTIFYMEDIA** notifie la fenêtre parente d’une application que le média a changé.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle vers la fenêtre MCIWnd.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Aid*
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nouveau nom de fichier. Si le média est en fermeture, il spécifie une chaîne NULL.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez activer la notification des modifications de média en spécifiant le \_ style de fenêtre MCIWNDF NOTIFYMEDIA.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





