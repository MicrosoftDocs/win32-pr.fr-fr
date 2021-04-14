---
title: Message RB_PUSHCHEVRON (commctrl. h)
description: Envoyé à un contrôle rebar pour pousser par programme un chevron.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508906"
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

## <a name="remarks"></a>Notes

Lorsque ce message est envoyé, le contrôle rebar envoie à l’application un code de notification [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , lui invitant à afficher le menu Chevron.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





