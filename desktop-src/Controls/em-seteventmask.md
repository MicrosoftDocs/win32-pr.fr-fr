---
title: Message EM_SETEVENTMASK (RichEdit. h)
description: Définit le masque d’événement pour un contrôle RichEdit. Le masque d’événement spécifie les codes de notification que le contrôle envoie à sa fenêtre parente.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- EM_SETEVENTMASK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244274d969473531bae7c1d124af24a88d6b98d9db8bdbe073d054a3a9e36ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048499"
---
# <a name="em_seteventmask-message"></a>\_Message em SETEVENTMASK

Définit le masque d’événement pour un contrôle RichEdit. Le masque d’événement spécifie les codes de notification que le contrôle envoie à sa fenêtre parente.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Nouveau masque d’événement pour le contrôle RichEdit. Pour obtenir la liste des masques d’événements, consultez [**indicateurs de masque d’événement de contrôle RichEdit**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne le masque d’événement précédent.

## <a name="remarks"></a>Remarques

Le masque d’événement par défaut (avant tout est défini) est ENM \_ aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETEVENTMASK em**](em-geteventmask.md)
</dt> <dt>

[**Indicateurs de masque d’événement de contrôle RichEdit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





