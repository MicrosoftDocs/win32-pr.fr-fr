---
title: Message EM_LIMITTEXT (winuser. h)
description: Définit la limite de texte d’un contrôle d’édition.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464902"
---
# <a name="em_limittext-message"></a>\_Message LIMITTEXT em

Définit la limite de texte d’un contrôle d’édition. La limite de texte correspond à la quantité maximale de texte, dans **TCHAR** s, que l’utilisateur peut taper dans le contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

Pour les contrôles d’édition et Microsoft Rich Edit 1,0, les octets sont utilisés. Pour Microsoft Rich Edit 2,0 et versions ultérieures, les caractères sont utilisés.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre maximal de **TCHAR** s que l’utilisateur peut entrer. Pour le texte ANSI, il s’agit du nombre d’octets ; pour le texte Unicode, il s’agit du nombre de caractères. Ce nombre n’inclut pas le caractère null de fin.

**Contrôles RichEdit :** Si ce paramètre est égal à zéro, la longueur du texte est définie sur 64 000 caractères.

Si ce paramètre est égal à zéro, la longueur du texte est définie sur 0x7FFFFFFE caractères pour les contrôles d’édition sur une seule ligne ou sur-1 pour les contrôles d’édition multiligne.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le **message \_ LIMITTEXT em** limite uniquement le texte que l’utilisateur peut entrer. Elle n’affecte pas le texte déjà présent dans le contrôle d’édition lorsque le message est envoyé, ni la longueur du texte copié dans le contrôle d’édition par le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) . Si une application utilise le message **WM \_ SETTEXT** pour placer plus de texte dans un contrôle d’édition que celui spécifié dans le message **em \_ LIMITTEXT** , l’utilisateur peut modifier tout le contenu du contrôle d’édition.

Avant l’appel de **em \_ LIMITTEXT** , la limite par défaut pour la quantité de texte qu’un utilisateur peut entrer dans un contrôle d’édition est de 32 767 caractères.

Pour les contrôles d’édition sur une seule ligne, la limite de texte est soit 0x7FFFFFFE octets, soit la valeur du paramètre *wParam* , selon celle qui est la plus petite. Pour les contrôles d’édition multilignes, cette valeur est soit-1 octet, soit la valeur du paramètre *wParam* , selon la valeur la plus petite.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Utilisez le message [**em \_ EXLIMITTEXT**](em-exlimittext.md) pour les valeurs de longueur de texte supérieures à 64 000. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_EXLIMITTEXT em**](em-exlimittext.md)
</dt> <dt>

[**Modifier \_ LimitText**](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

