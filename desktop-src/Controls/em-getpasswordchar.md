---
title: Message EM_GETPASSWORDCHAR (winuser. h)
description: Obtient le caractère de mot de passe qu’un contrôle d’édition affiche lorsque l’utilisateur entre du texte. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c4e7ac576f18d0ab28fcf8c2288d2bee7966866a71180a81c34896c2396f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831205"
---
# <a name="em_getpasswordchar-message"></a>\_Message GETPASSWORDCHAR em

Obtient le caractère de mot de passe qu’un contrôle d’édition affiche lorsque l’utilisateur entre du texte. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

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

La valeur de retour spécifie le caractère à afficher à la place des caractères tapés par l’utilisateur. Si la valeur de retour est **null**, il n’y a pas de caractère de mot de passe et le contrôle affiche les caractères tapés par l’utilisateur.

## <a name="remarks"></a>Remarques

Si un contrôle d’édition est créé avec le style [**\_ de mot de passe es**](edit-control-styles.md) , le caractère de mot de passe par défaut est défini sur un astérisque ( \* ). Si un contrôle d’édition est créé sans le style **\_ de mot de passe es** , il n’y a pas de caractère de mot de passe. Pour modifier le mot de passe, envoyez le message [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md) .

**Contrôles d’édition :** Les contrôles d’édition multiligne ne prennent pas en charge le style ou les messages de mot de passe.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 2,0 et versions ultérieures. Les contrôles d’édition sur une seule ligne et sur plusieurs lignes prennent en charge le style et les messages du mot de passe. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETPASSWORDCHAR em**](em-setpasswordchar.md)
</dt> </dl>

 

 





