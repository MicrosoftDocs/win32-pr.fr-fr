---
title: Message BCM_SETNOTE (commctrl. h)
description: Définit le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ SetNote macro.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920395"
---
# <a name="bcm_setnote-message"></a>\_Message SETNOTE BCM

Définit le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne **WCHAR** se terminant par un caractère null qui contient la note.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

À partir de la version 6,01 de ComCtl32, les boutons de lien de commande peuvent avoir une note.

Le **message \_ SETNOTE BCM** fonctionne uniquement avec les styles de bouton [**BS \_ COMMANDLINK**](button-styles.md) et [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





