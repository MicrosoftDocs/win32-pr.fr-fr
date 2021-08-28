---
title: Message EM_FMTLINES (winuser. h)
description: Définit un indicateur qui détermine si un contrôle d’édition multiligne contient des caractères de saut de ligne conditionnels. Un saut de ligne conditionnel se compose de deux retours chariot et d’un saut de ligne et est inséré à la fin d’une ligne qui est cassée en raison de wordwrapping.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e0c0c410f13a33f0e387098178b42faaf3269c36d11f75e765eb753fa9d0844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545099"
---
# <a name="em_fmtlines-message"></a>\_Message FMTLINES em

Définit un indicateur qui détermine si un contrôle d’édition multiligne contient des caractères de saut de ligne conditionnels. Un saut de ligne conditionnel se compose de deux retours chariot et d’un saut de ligne et est inséré à la fin d’une ligne qui est cassée en raison de wordwrapping.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si les caractères de saut de ligne conditionnel doivent être insérés. La valeur **true** insère les caractères ; la valeur **false** les supprime.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est identique au paramètre *wParam* .

## <a name="remarks"></a>Remarques

Ce message affecte uniquement la mémoire tampon retournée par le message [**em \_ GETHANDLE**](em-gethandle.md) et le texte retourné par le message [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) . Elle n’a aucun effet sur l’affichage du texte dans le contrôle d’édition.

Le **message \_ FMTLINES em** n’affecte pas une ligne qui se termine par un saut de ligne matériel. Un saut de ligne matériel consiste en un retour chariot et un saut de ligne.

> [!Note]  
> Taille du texte modifié lors du traitement de ce message.

 

**Modification riche :** Le **message \_ FMTLINES em** n’est pas pris en charge.

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

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

