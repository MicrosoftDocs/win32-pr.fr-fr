---
title: Message TBM_GETTHUMBRECT (commctrl. h)
description: Récupère la taille et la position du rectangle englobant pour le curseur dans un TrackBar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032883"
---
# <a name="tbm_getthumbrect-message"></a>\_Message TBM GETTHUMBRECT

Récupère la taille et la position du rectangle englobant pour le curseur dans un TrackBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) . Le message remplit cette structure à l’aide du rectangle englobant du curseur de la barre de défilement dans les coordonnées clientes de la fenêtre du TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

