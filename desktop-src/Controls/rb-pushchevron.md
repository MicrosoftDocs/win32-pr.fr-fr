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
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117246"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Lorsque ce message est envoyé, le contrôle rebar envoie à l’application un code de notification [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , lui invitant à afficher le menu Chevron.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





