---
title: Message EM_GETCTFOPENSTATUS (RichEdit. h)
description: Détermine si le clavier de l’infrastructure TSF (Text Services Framework) est ouvert ou fermé.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006486"
---
# <a name="em_getctfopenstatus-message"></a>\_Message GETCTFOPENSTATUS em

Détermine si le clavier de l’infrastructure TSF (Text Services Framework) est ouvert ou fermé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le clavier TSF est ouvert, la valeur de retour est **true**. Sinon, la **valeur est false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETCTFOPENSTATUS em**](em-setctfopenstatus.md)
</dt> </dl>

 

 





