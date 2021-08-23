---
title: Message EM_GETRECT (winuser. h)
description: Obtient le rectangle de mise en forme d’un contrôle d’édition.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d4ad7dbab40a8d294d814e3524b54c5b11206c91608e9293bdf88df2a63f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541039"
---
# <a name="em_getrect-message"></a>\_Message GETRECT em

Obtient le [rectangle de mise en forme](about-edit-controls.md) d’un contrôle d’édition. Le rectangle de mise en forme est le rectangle de limitation dans lequel le contrôle dessine le texte. Le rectangle de limitation est indépendant de la taille de la fenêtre Modifier-contrôle. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle de mise en forme.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas significative.

## <a name="remarks"></a>Remarques

Vous pouvez modifier le rectangle de mise en forme d’un contrôle d’édition multiligne à l’aide des messages [**em \_ SETRECT**](em-setrect.md) et [**em \_ SETRECTNP**](em-setrectnp.md) .

Dans certaines conditions, **em \_ GETRECT** peut ne pas retourner les valeurs exactes pour lesquelles [**em \_ SETRECT**](em-setrect.md) ou [**em \_ SETRECTNP**](em-setrectnp.md) est approximativement correct, mais il peut être décalé de quelques pixels.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Le rectangle de mise en forme n’inclut pas la barre de sélection, qui est une zone non marquée à gauche de chaque paragraphe. Lorsque vous cliquez sur cette option, la barre de sélection sélectionne la ligne. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[**\_SETRECT em**](em-setrect.md)
</dt> <dt>

[**\_SETRECTNP em**](em-setrectnp.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

