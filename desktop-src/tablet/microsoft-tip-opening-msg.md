---
description: Avertit la fenêtre de l’ouverture du panneau de saisie de texte.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Message MICROSOFT_TIP_OPENING_MSG (PenInputPanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530023"
---
# <a name="microsoft_tip_opening_msg-message"></a>\_Conseil Microsoft \_ ouverture du \_ message MSG

Avertit la fenêtre de l’ouverture du panneau de saisie de texte.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

N’est pas utilisé actuellement, doit avoir la **valeur null**.

</dd> <dt>

*lParam* 
</dt> <dd>

N’est pas utilisé actuellement, doit avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Les applications doivent appeler [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) après le traitement de ce message. Pour plus d’informations sur les valeurs de retour, consultez **DefWindowProc** .

## <a name="remarks"></a>Notes

Cette notification vous permet de savoir à quel moment le panneau de saisie s’ouvre. Si vous souhaitez exécuter une action lorsque cela se produit, gérez le message, effectuez votre opération dans le gestionnaire, puis transmettez le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Ce message est également envoyé lorsque le panneau de saisie de texte est déjà visible et que l’utilisateur passe du clavier à l’apparence d’écriture manuscrite.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista<br/>                                                                   |
| En-tête<br/> | <dl> <dt>PenInputPanel. h</dt> </dl> |



 

