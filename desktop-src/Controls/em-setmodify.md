---
title: Message EM_SETMODIFY (winuser. h)
description: Définit ou efface l’indicateur de modification d’un contrôle d’édition. L’indicateur de modification indique si le texte du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006380"
---
# <a name="em_setmodify-message"></a>\_Message SETMODIFY em

Définit ou efface l’indicateur de modification d’un contrôle d’édition. L’indicateur de modification indique si le texte du contrôle d’édition a été modifié. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouvelle valeur de l’indicateur de modification. La valeur **true** indique que le texte a été modifié et la valeur **false** indique qu’il n’a pas été modifié.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le système efface automatiquement l’indicateur de modification à zéro lorsque le contrôle est créé. Si l’utilisateur modifie le texte du contrôle, le système affecte à l’indicateur une valeur différente de zéro. Vous pouvez envoyer le [**message \_ GETMODIFY em**](em-getmodify.md) au contrôle d’édition pour récupérer l’état actuel de l’indicateur.

**Édition enrichie 1,0 :** Les objets créés sans l’indicateur **REO \_ Dynamics** sont verrouillés dans leurs étendues lorsque l’indicateur de modification est défini sur **false**.

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

[**\_GETMODIFY em**](em-getmodify.md)
</dt> <dt>

[**Réobjet**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





