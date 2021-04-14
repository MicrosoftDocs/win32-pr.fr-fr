---
title: Message HDM_GETOVERFLOWRECT (commctrl. h)
description: Obtient le rectangle englobant du bouton de dépassement de capacité lorsque le \_ style de dépassement de capacité HDS est défini sur le contrôle d’en-tête et que le bouton de dépassement de capacité est visible. Envoyez ce message de manière explicite ou à l’aide de la macro GetOverflowRect d’en-tête \_ .
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508802"
---
# <a name="hdm_getoverflowrect-message"></a>\_Message HDM GETOVERFLOWRECT

Obtient le rectangle englobant du bouton de dépassement de capacité lorsque le style de [**\_ dépassement de capacité HDS**](header-control-styles.md) est défini sur le contrôle d’en-tête et que le bouton de dépassement de capacité est visible. Envoyez ce message de manière explicite ou à l’aide de la macro [**\_ GetOverflowRect d’en-tête**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé. Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour recevoir les informations de rectangle englobant. L’expéditeur du message est chargé d’allouer cette structure. Les coordonnées retournées dans la structure **Rect** sont exprimées en tant que coordonnées d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ; Sinon, **false**.

## <a name="remarks"></a>Notes

Le contrôle header doit avoir le style **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos des contrôles Header](header-controls.md)
</dt> </dl>

 

