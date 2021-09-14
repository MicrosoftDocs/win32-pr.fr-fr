---
title: Message SB_GETBORDERS (commctrl. h)
description: Récupère les largeurs actuelles des bordures horizontale et verticale d’une fenêtre d’État.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117113"
---
# <a name="sb_getborders-message"></a>\_Message SB GETBORDERS

Récupère les largeurs actuelles des bordures horizontale et verticale d’une fenêtre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau d’entiers qui a trois éléments. Le premier élément reçoit la largeur de la bordure horizontale, le deuxième reçoit la largeur de la bordure verticale et le troisième reçoit la largeur de la bordure entre les rectangles.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Les bordures déterminent l’espacement entre le bord extérieur de la fenêtre et les rectangles de la fenêtre qui contiennent du texte. Les bordures déterminent également l’espacement entre les rectangles.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





