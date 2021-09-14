---
title: Message LB_SETITEMHEIGHT (winuser. h)
description: Définit la hauteur, en pixels, des éléments d’une zone de liste. Si la zone de liste présente le \_ style OWNERDRAWVARIABLE, ce message définit la hauteur de l’élément spécifié par le paramètre wParam. Dans le cas contraire, ce message définit la hauteur de tous les éléments de la zone de liste.
ms.assetid: 3ac8e935-6de8-465f-a525-1f493b06ee7c
keywords:
- LB_SETITEMHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9985c5131a9eb1c8f0c45b6ab399b9e270f962cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999854"
---
# <a name="lb_setitemheight-message"></a>\_Message SETITEMHEIGHT lb

Définit la hauteur, en pixels, des éléments d’une zone de liste. Si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) , ce message définit la hauteur de l’élément spécifié par le paramètre *wParam* . Dans le cas contraire, ce message définit la hauteur de tous les éléments de la zone de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro de l’élément dans la zone de liste. Utilisez ce paramètre uniquement si la zone de liste présente le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) . sinon, affectez-lui la valeur zéro.

Windows 95/Windows 98/Windows Millennium edition (Windows) : le paramètre *wParam* est limité aux valeurs 16 bits. Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments. Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la hauteur, en pixels, de l’élément. La hauteur maximale est de 255 pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’index ou la hauteur n’est pas valide, la valeur de retour est LB \_ Err.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETITEMHEIGHT lb**](lb-getitemheight.md)
</dt> </dl>

 

 





