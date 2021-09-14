---
title: Message TB_SETBUTTONWIDTH (commctrl. h)
description: Définit les largeurs minimale et maximale des boutons dans le contrôle ToolBar.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116597"
---
# <a name="tb_setbuttonwidth-message"></a>TO \_ SETBUTTONWIDTH message

Définit les largeurs minimale et maximale des boutons dans le contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la largeur minimale du bouton, en pixels. Les boutons de la barre d’outils ne seront jamais plus étroits que cette valeur.

Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la largeur maximale du bouton, en pixels. Si le texte du bouton est trop grand, le contrôle l’affiche avec des points de suspension.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Utilisez **to \_ SETBUTTONWIDTH** pour définir les largeurs maximales et minimales autorisées pour les boutons avant leur ajout. Utilisez [**to \_ SETBUTTONSIZE**](tb-setbuttonsize.md) pour définir la taille réelle des boutons.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

