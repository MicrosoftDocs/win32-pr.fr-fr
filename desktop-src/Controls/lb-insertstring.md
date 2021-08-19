---
title: Message LB_INSERTSTRING (winuser. h)
description: Insère une chaîne ou des données d’élément dans une zone de liste. Contrairement au \_ message lb ADDSTRING, le \_ message INSERTSTRING ne provoque pas le tri d’une liste avec le style de tri lbs \_ .
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd47d08ef78c590ecb3b5900143b29bc49676b86d8facdcc91b05bb34c8f4aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085389"
---
# <a name="lb_insertstring-message"></a>\_Message INSERTSTRING lb

Insère une chaîne ou des données d’élément dans une zone de liste. Contrairement au message [**lb \_ ADDSTRING**](lb-addstring.md) , le **message \_ INSERTSTRING** ne provoque pas le tri d’une liste avec le style de [**\_ Tri lbs**](list-box-styles.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la position à laquelle insérer la chaîne. Si ce paramètre a la valeur-1, la chaîne est ajoutée à la fin de la liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null à insérer. Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , ce paramètre est stocké en tant que données d’élément au lieu d’une chaîne. Vous pouvez envoyer les messages [**lb \_ GETITEMDATA**](lb-getitemdata.md) et [**\_ SETITEMDATA**](lb-setitemdata.md) pour extraire ou modifier les données de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de la position à laquelle la chaîne a été insérée. Si une erreur se produit, la valeur de retour est LB \_ Err. Si l’espace est insuffisant pour stocker la nouvelle chaîne, la valeur de retour est LB \_ ERRSPACE.

## <a name="remarks"></a>Remarques

Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100). Il réserve la quantité de mémoire spécifiée afin que les **messages \_ INSERTSTRING** suivants prennent le plus rapidement possible. Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* . Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.

Si la zone de liste a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous insérez une chaîne plus grande que la zone de liste, envoyez un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.

Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP. Cela peut entraîner des problèmes. par exemple, les caractères romains accentués dans une zone de liste non Unicode en japonais Windows sont tronqués. Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**\_SELECTSTRING lb**](lb-selectstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> </dl>

 

