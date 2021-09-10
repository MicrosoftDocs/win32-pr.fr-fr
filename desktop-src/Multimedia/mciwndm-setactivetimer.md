---
title: Message MCIWNDM_SETACTIVETIMER (VFW. h)
description: Le \_ message MCIWNDM SETACTIVETIMER définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est active. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- message MCIWNDM_SETACTIVETIMER Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364319"
---
# <a name="mciwndm_setactivetimer-message"></a>\_Message MCIWNDM SETACTIVETIMER

Le message **MCIWNDM \_ SETACTIVETIMER** définit la période de mise à jour utilisée par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente lorsque la fenêtre MCIWnd est active. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*proactive*
</dt> <dd>

Période de mise à jour, en millisecondes. La valeur par défaut est 500 millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





