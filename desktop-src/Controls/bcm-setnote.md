---
title: Message BCM_SETNOTE (commctrl. h)
description: Définit le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ SetNote macro.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942116"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

À partir de la version 6,01 de ComCtl32, les boutons de lien de commande peuvent avoir une note.

Le **message \_ SETNOTE BCM** fonctionne uniquement avec les styles de bouton [**BS \_ COMMANDLINK**](button-styles.md) et [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

 





