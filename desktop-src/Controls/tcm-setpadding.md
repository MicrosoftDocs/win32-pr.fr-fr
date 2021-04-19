---
title: Message TCM_SETPADDING (commctrl. h)
description: Définit la quantité d’espace (remplissage) autour de l’icône et de l’étiquette de chaque onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING les contrôles de message Windows
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
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531609"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

