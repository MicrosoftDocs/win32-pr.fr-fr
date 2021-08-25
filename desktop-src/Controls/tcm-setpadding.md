---
title: Message TCM_SETPADDING (commctrl. h)
description: Définit la quantité d’espace (remplissage) autour de l’icône et de l’étiquette de chaque onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969ae3c7c240c38a6643682321c14e5744f2d2c2eec188004d1c3b2e6f2b3835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876239"
---
# <a name="tcm_setpadding-message"></a>\_Message SETPADDING TCM

Définit la quantité d’espace (remplissage) autour de l’icône et de l’étiquette de chaque onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est une valeur **int** qui spécifie la quantité de remplissage horizontal, en pixels. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est une valeur **int** qui spécifie la quantité de remplissage vertical, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

