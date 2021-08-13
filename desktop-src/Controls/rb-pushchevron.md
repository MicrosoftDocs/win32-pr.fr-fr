---
title: Message RB_PUSHCHEVRON (commctrl. h)
description: Envoyé à un contrôle rebar pour pousser par programme un chevron.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d095cd824970b7ea90541420274b204a1e2f63ce6e1218e62221741f572feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434969"
---
# <a name="rb_pushchevron-message"></a>\_Message PUSHCHEVRON RB

Envoyé à un contrôle rebar pour pousser par programme un chevron.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la bande dont le Chevron doit faire l’objet d’un push.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur 32 bits définie par l’application. Elle est repassée à l’application en tant que membre **lParamNM** de la structure [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) qui est passée avec la notification [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Remarques

Lorsque ce message est envoyé, le contrôle rebar envoie à l’application un code de notification [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , lui invitant à afficher le menu Chevron.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





