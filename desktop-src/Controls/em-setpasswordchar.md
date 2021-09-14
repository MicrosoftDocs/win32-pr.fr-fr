---
title: Message EM_SETPASSWORDCHAR (winuser. h)
description: Définit ou supprime le caractère de mot de passe pour un contrôle d’édition. Lorsqu’un caractère de mot de passe est défini, ce caractère est affiché à la place des caractères tapés par l’utilisateur. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006365"
---
# <a name="em_setpasswordchar-message"></a>\_Message SETPASSWORDCHAR em

Définit ou supprime le caractère de mot de passe pour un contrôle d’édition. Lorsqu’un caractère de mot de passe est défini, ce caractère est affiché à la place des caractères tapés par l’utilisateur. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Caractère à afficher à la place des caractères tapés par l’utilisateur. Si ce paramètre est égal à zéro, le contrôle supprime le caractère de mot de passe actuel et affiche les caractères tapés par l’utilisateur.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsqu’un contrôle d’édition reçoit le message **\_ SETPASSWORDCHAR em** , le contrôle redessine tous les caractères visibles à l’aide du caractère spécifié par le paramètre *wParam* . Si *wParam* est égal à zéro, le contrôle redessine tous les caractères visibles à l’aide des caractères tapés par l’utilisateur.

Si un contrôle d’édition est créé avec le style [**\_ de mot de passe es**](edit-control-styles.md) , le caractère de mot de passe par défaut est défini sur un astérisque ( \* ). Si un contrôle d’édition est créé sans le style **\_ de mot de passe es** , il n’y a pas de caractère de mot de passe. Le **style \_ de mot de passe es** est supprimé si un message **\_ SETPASSWORDCHAR em** est envoyé avec le paramètre *wParam* défini sur zéro.

**Contrôles d’édition :** Les contrôles d’édition multiligne ne prennent pas en charge le style ou les messages de mot de passe.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 2,0 et versions ultérieures. Les contrôles d’édition sur une seule ligne et sur plusieurs lignes prennent en charge le style et les messages du mot de passe. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETPASSWORDCHAR em**](em-getpasswordchar.md)
</dt> </dl>

 

 





