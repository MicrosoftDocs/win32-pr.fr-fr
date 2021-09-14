---
title: Message EM_SETREADONLY (winuser. h)
description: Définit ou supprime le style en lecture seule (ES \_ ReadOnly) d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006363"
---
# <a name="em_setreadonly-message"></a>\_Message SETREADONLY em

Définit ou supprime le style en lecture seule ([**es \_ ReadOnly**](edit-control-styles.md)) d’un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie s’il faut définir ou supprimer le style [**es \_ ReadOnly**](edit-control-styles.md) . La valeur **true** définit le style **es \_ ReadOnly** ; la valeur **false** supprime le style **es \_ ReadOnly** .

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération a échoué, la valeur de retour est différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Lorsqu’un contrôle d’édition a le style [**es \_ ReadOnly**](edit-control-styles.md) , l’utilisateur ne peut pas modifier le texte dans le contrôle d’édition.

Pour déterminer si un contrôle d’édition a le style [**es \_ ReadOnly**](edit-control-styles.md) , utilisez la fonction [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) avec l' \_ indicateur de style GWL.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

