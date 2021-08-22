---
title: Message TBM_SETTICFREQ (commctrl. h)
description: Définit la fréquence d’intervalle des graduations d’un TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c1b3e029abc8027d8708da31698f44db85ec78e427ba9461f0a71a740fb05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078013"
---
# <a name="tbm_setticfreq-message"></a>\_Message TBM SETTICFREQ

Définit la fréquence d’intervalle des graduations d’un TrackBar. Par exemple, si la fréquence est définie sur deux, une graduation est affichée pour chaque autre incrément dans la plage du TrackBar. Le paramètre par défaut de la fréquence est un ; autrement dit, chaque incrément de la plage est associé à une graduation.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Fréquence des graduations.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Le TrackBar doit avoir le style des [**\_ graduations tbs**](trackbar-control-styles.md) pour utiliser ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





