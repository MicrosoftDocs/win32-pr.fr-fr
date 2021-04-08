---
title: Message EM_GETMODIFY (winuser. h)
description: Obtient l’état de l’indicateur de modification d’un contrôle d’édition. L’indicateur indique si le contenu du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY les contrôles de message Windows
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
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843205"
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

## <a name="remarks"></a>Notes

Le système efface automatiquement l’indicateur de modification à zéro lorsque le contrôle est créé. Si l’utilisateur modifie le texte du contrôle, le système affecte à l’indicateur une valeur différente de zéro. Vous pouvez envoyer le [**message \_ SETMODIFY em**](em-setmodify.md) au contrôle Edit pour définir ou supprimer l’indicateur.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETMODIFY em**](em-setmodify.md)
</dt> </dl>

 

 





