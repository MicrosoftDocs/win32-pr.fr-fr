---
title: Message TBM_SETTICFREQ (commctrl. h)
description: Définit la fréquence d’intervalle des graduations d’un TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ les contrôles de message Windows
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
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032610"
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

## <a name="remarks"></a>Notes

Le TrackBar doit avoir le style des [**\_ graduations tbs**](trackbar-control-styles.md) pour utiliser ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





