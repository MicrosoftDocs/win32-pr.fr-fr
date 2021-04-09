---
title: Message EM_STOPGROUPTYPING (RichEdit. h)
description: Empêche un contrôle RichEdit de collecter des actions de frappe supplémentaires dans l’action d’annulation actuelle. Le contrôle stocke l’action de frappe suivante, le cas échéant, dans une nouvelle action de la file d’attente d’annulation.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741236"
---
# <a name="em_stopgrouptyping-message"></a>\_Message STOPGROUPTYPING em

Empêche un contrôle RichEdit de collecter des actions de frappe supplémentaires dans l’action d’annulation actuelle. Le contrôle stocke l’action de frappe suivante, le cas échéant, dans une nouvelle action de la file d’attente d’annulation.

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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est égale à zéro. Ce message ne peut pas échouer.

## <a name="remarks"></a>Notes

Un contrôle RichEdit regroupe les actions consécutives de frappe, y compris les caractères supprimés à l’aide de la touche **retour arrière** , en une seule opération d’annulation jusqu’à ce que l’un des événements suivants se produise :

-   Le contrôle reçoit un **message \_ STOPGROUPTYPING em** .
-   Le contrôle perd le focus.
-   L’utilisateur déplace la sélection actuelle, soit à l’aide des touches de direction, soit en cliquant sur la souris.
-   L’utilisateur appuie sur la touche **Suppr** .
-   L’utilisateur effectue toute autre action, telle qu’une opération de collage qui n’implique **pas** de saisie.

Vous pouvez envoyer le **message \_ STOPGROUPTYPING em** pour fractionner les actions de frappe consécutives en groupes d’annulation plus petits. Par exemple, vous pouvez envoyer **des \_ STOPGROUPTYPING em** après chaque caractère ou à chaque saut de mot.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Effacer em**](em-undo.md)
</dt> </dl>

 

 





