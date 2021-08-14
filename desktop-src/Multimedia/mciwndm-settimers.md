---
title: Message MCIWNDM_SETTIMERS (VFW. h)
description: Le \_ message MCIWNDM SETTIMERS définit les périodes de mise à jour utilisées par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- message MCIWNDM_SETTIMERS Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9c17a131827459555ae51adc5d5bd48d98fabb88fc4c1f0dbbcd1eb3673466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807553"
---
# <a name="mciwndm_settimers-message"></a>\_Message MCIWNDM SETTIMERS

Le message **MCIWNDM \_ SETTIMERS** définit les périodes de mise à jour utilisées par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*proactive*
</dt> <dd>

Période de mise à jour utilisée par MCIWnd lorsqu’il s’agit de la fenêtre active. La valeur par défaut est 500 millisecondes. Stockage pour cette valeur est limité à 16 bits.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inactive*
</dt> <dd>

Période de mise à jour utilisée par MCIWnd lorsqu’il s’agit de la fenêtre inactive. La valeur par défaut est 2000 millisecondes. Stockage pour cette valeur est limité à 16 bits.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





