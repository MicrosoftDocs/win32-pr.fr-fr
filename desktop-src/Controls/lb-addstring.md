---
title: Message LB_ADDSTRING (winuser. h)
description: Ajoute une chaîne à une zone de liste. Si la zone de liste n’a pas le \_ style de tri lbs, la chaîne est ajoutée à la fin de la liste. Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552e3c344a730ad1fc00337cafa71a19a6586b9a4c95f2ed1ebce352d9d909aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671685"
---
# <a name="lb_addstring-message"></a>Message g LB \_

Ajoute une chaîne à une zone de liste. Si la zone de liste n’a pas le style de [**\_ Tri lbs**](list-box-styles.md) , la chaîne est ajoutée à la fin de la liste. Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la chaîne terminée par le caractère null qui doit être ajoutée.

Si la zone de liste a un style owner-drawn, mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , ce paramètre est stocké en tant que données d’élément au lieu d’une chaîne. Vous pouvez envoyer les messages **lb \_ GETITEMDATA** et **\_ SETITEMDATA** pour extraire ou modifier les données de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’index de base zéro de la chaîne dans la zone de liste. Si une erreur se produit, la valeur de retour est LB \_ Err. Si l’espace est insuffisant pour stocker la nouvelle chaîne, la valeur de retour est LB \_ ERRSPACE.

## <a name="remarks"></a>Remarques

Si la zone de liste a un style owner-drawn et le style de [**\_ Tri lbs**](list-box-styles.md) , mais pas le style [**\_ HASSTRINGS kg**](list-box-styles.md) , le système envoie une ou plusieurs fois le message [**WM \_ COMPAREITEM**](wm-compareitem.md) au propriétaire de la zone de liste pour placer correctement le nouvel élément dans la zone de liste.

Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100). Il réserve la quantité de mémoire spécifiée, de sorte **que \_ les messages de** l’équilibreur de volume suivant prennent le plus de temps possible. Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* . Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.

Si la zone de liste a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous ajoutez une chaîne plus grande que la zone de liste, envoyez un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.

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

[**\_DELETESTRING lb**](lb-deletestring.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> <dt>

[**\_SELECTSTRING lb**](lb-selectstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_COMPAREITEM WM**](wm-compareitem.md)
</dt> </dl>

 

