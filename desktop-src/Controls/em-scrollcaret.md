---
title: Message EM_SCROLLCARET (winuser. h)
description: Fait défiler le signe insertion dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- EM_SCROLLCARET les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006428"
---
# <a name="em_scrollcaret-message"></a>\_Message SCROLLCARET em

Fait défiler le signe insertion dans un contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre est réservé. Elle doit être définie sur zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre est réservé. Elle doit être définie sur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour n’est pas significative.

## <a name="remarks"></a>Notes

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_LINESCROLL em**](em-linescroll.md)
</dt> <dt>

[**\_défilement em**](em-scroll.md)
</dt> <dt>

[**\_VSCROLL WM**](wm-vscroll.md)
</dt> </dl>

 

 





