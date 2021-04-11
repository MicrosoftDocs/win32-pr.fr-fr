---
title: Message TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indique si la barre de progression hébergée d’une boîte de dialogue de tâche doit être affichée en mode palissade.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105970"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>\_Message de \_ barre de \_ progression du texte défilant de l’ensemble TDM \_

Indique si la barre de progression hébergée d’une boîte de dialogue de tâche doit être affichée en mode palissade.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui indique si la barre de progression doit être affichée en mode texte défilant. La valeur **true** active le mode texte défilant, tandis que la valeur **false** désactive le mode texte défilant.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Pour plus d’informations sur le mode texte défilant, consultez [contrôle de barre de progression](progress-bar-control.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





