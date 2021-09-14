---
title: Message EM_SETLIMITTEXT (winuser. h)
description: 'EM_SETLIMITTEXT message : définit la limite de texte d’un contrôle d’édition.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006382"
---
# <a name="em_setlimittext-message"></a>\_Message SETLIMITTEXT em

Définit la limite de texte d’un contrôle d’édition. La limite de texte correspond à la quantité maximale de texte, dans **TCHAR** s, que l’utilisateur peut taper dans le contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

Pour les contrôles d’édition et Microsoft Rich Edit 1,0, les octets sont utilisés. Pour Microsoft Rich Edit 2,0 et versions ultérieures, les caractères sont utilisés.

Le **message \_ SETLIMITTEXT em** est identique au message [**em \_ LIMITTEXT**](em-limittext.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre maximal de **TCHAR** s que l’utilisateur peut entrer. Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères. Ce nombre n’inclut pas le caractère null de fin.

**Contrôles RichEdit :** Si ce paramètre est égal à zéro, la longueur du texte est définie sur 64 000 caractères.

Si ce paramètre est égal à zéro, la longueur du texte est définie sur 0x7FFFFFFE caractères pour les contrôles d’édition sur une seule ligne ou sur 1 pour les contrôles d’édition multiligne.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le **message \_ SETLIMITTEXT em** limite uniquement le texte que l’utilisateur peut entrer. Elle n’affecte pas le texte déjà présent dans le contrôle d’édition lorsque le message est envoyé, ni la longueur du texte copié dans le contrôle d’édition par le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . Si une application utilise le message **WM \_ SETTEXT** pour placer plus de texte dans un contrôle d’édition que celui spécifié dans le message **em \_ SETLIMITTEXT** , l’utilisateur peut modifier tout le contenu du contrôle d’édition.

Avant l’appel de **em \_ SETLIMITTEXT** , la limite par défaut pour la quantité de texte qu’un utilisateur peut entrer dans un contrôle d’édition est de 32 767 caractères.

Pour les contrôles d’édition sur une seule ligne, la limite de texte est soit 0x7FFFFFFE octets, soit la valeur du paramètre *wParam* , selon celle qui est la plus petite. Pour les contrôles d’édition multiligne, cette valeur est soit 1 octet, soit la valeur du paramètre *wParam* , selon celle qui est la plus petite.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Utilisez le message [**em \_ EXLIMITTEXT**](em-exlimittext.md) pour les valeurs de longueur de texte supérieures à 64 000. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETLIMITTEXT em**](em-getlimittext.md)
</dt> </dl>

 

