---
title: Message LB_SETHORIZONTALEXTENT (winuser. h)
description: Définit la largeur, en pixels, à laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999855"
---
# <a name="lb_sethorizontalextent-message"></a>\_Message SETHORIZONTALEXTENT lb

Définit la largeur, en pixels, à laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement). Si la largeur de la zone de liste est inférieure à cette valeur, la barre de défilement horizontale fait défiler horizontalement les éléments de la zone de liste. Si la largeur de la zone de liste est supérieure ou égale à cette valeur, la barre de défilement horizontale est masquée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le nombre de pixels utilisés pour faire défiler la zone de liste.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour répondre au message **lb \_ SETHORIZONTALEXTENT** , la zone de liste doit avoir été définie avec le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Notez qu’une zone de liste ne met pas à jour son étendue horizontale de manière dynamique.

Ce message n’a aucun effet sur une zone de liste à plusieurs colonnes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md)
</dt> </dl>

 

