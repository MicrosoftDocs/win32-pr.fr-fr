---
title: Message EM_GETLINECOUNT (winuser. h)
description: Obtient le nombre de lignes dans un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44487084da8df8edd463fc0683c9d27fcba19a2993465e5493edfd8bb7c3c6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006682"
---
# <a name="em_getlinecount-message-winuserh"></a>Message EM_GETLINECOUNT (winuser. h)

Obtient le nombre de lignes dans un contrôle d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

La valeur de retour est un entier spécifiant le nombre total de lignes de texte dans le contrôle d’édition multiligne ou le contrôle Rich Edit. Si le contrôle n’a pas de texte, la valeur de retour est 1. La valeur de retour ne sera jamais inférieure à 1.

## <a name="remarks"></a>Remarques

Le message **em \_ GETLINECOUNT** récupère le nombre total de lignes de texte, pas seulement le nombre de lignes actuellement visibles.

Si la fonctionnalité de retour automatique à la ligne est activée, le nombre de lignes peut changer lorsque les dimensions de la fenêtre d’édition changent.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETLINE em**](em-getline.md)
</dt> <dt>

[**\_LINELENGTH em**](em-linelength.md)
</dt> <dt>

[**Modifier \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





