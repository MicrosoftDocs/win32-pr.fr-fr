---
title: Message LB_SETCARETINDEX (winuser. h)
description: Définit le rectangle de focus sur l’élément à l’index spécifié dans une zone de liste à sélection multiple. Si l’élément n’est pas visible, il fait l’objet d’un défilement dans la vue.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- LB_SETCARETINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999857"
---
# <a name="lb_setcaretindex-message"></a>\_Message SETCARETINDEX lb

Définit le rectangle de focus sur l’élément à l’index spécifié dans une zone de liste à sélection multiple. Si l’élément n’est pas visible, il fait l’objet d’un défilement dans la vue.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro de l’élément de zone de liste qui doit recevoir le rectangle de focus.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Si cette valeur est **false**, l’élément fait l’objet d’un défilement jusqu’à ce qu’il soit entièrement visible. Si la **valeur est true**, l’élément fait l’objet d’un défilement jusqu’à ce qu’il soit au moins partiellement visible.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une erreur se produit, la valeur de retour est LB \_ Err (-1). Dans le cas contraire, LB \_ Okay (0) est retourné.

## <a name="remarks"></a>Notes

Si ce message est envoyé à une zone de liste à sélection unique qui ne contient pas d’élément sélectionné, l’index du signe insertion est défini sur l’élément spécifié par le paramètre *wParam* . Si la zone de liste à sélection unique contient un élément sélectionné, la zone de liste retourne LB \_ Err.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> </dl>

 

 





