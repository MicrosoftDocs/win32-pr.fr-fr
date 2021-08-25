---
title: Message EM_GETMODIFY (winuser. h)
description: Obtient l’état de l’indicateur de modification d’un contrôle d’édition. L’indicateur indique si le contenu du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34156e363824e975af68449b40ed639eeeb7e3ab76bd680b9837f3d3dd907537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048899"
---
# <a name="em_getmodify-message"></a>\_Message GETMODIFY em

Obtient l’état de l’indicateur de modification d’un contrôle d’édition. L’indicateur indique si le contenu du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

Si le contenu du contrôle d’édition a été modifié, la valeur de retour est différente de zéro ; dans le cas contraire, il est égal à zéro.

## <a name="remarks"></a>Remarques

Le système efface automatiquement l’indicateur de modification à zéro lorsque le contrôle est créé. Si l’utilisateur modifie le texte du contrôle, le système affecte à l’indicateur une valeur différente de zéro. Vous pouvez envoyer le [**message \_ SETMODIFY em**](em-setmodify.md) au contrôle Edit pour définir ou supprimer l’indicateur.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETMODIFY em**](em-setmodify.md)
</dt> </dl>

 

 





