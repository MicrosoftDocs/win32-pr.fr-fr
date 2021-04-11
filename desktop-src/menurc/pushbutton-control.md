---
title: Contrôle PUSHBUTTON (menus et autres ressources)
description: Définit un contrôle de bouton de commande. Le contrôle est un rectangle à angles arrondis contenant le texte donné. Le texte est centré dans le contrôle. Le contrôle envoie un message à son parent chaque fois que l’utilisateur choisit le contrôle.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menus du contrôle de bouton de commande et autres ressources
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315131"
---
# <a name="pushbutton-control"></a>Contrôle PUSHBUTTON

Définit un contrôle de bouton de commande. Le contrôle est un rectangle à angles arrondis contenant le texte donné. Le texte est centré dans le contrôle. Le contrôle envoie un message à son parent chaque fois que l’utilisateur choisit le contrôle.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles pour le bouton de commande, qui peuvent être une combinaison du style de la **BS- \_ PUSHBUTTON** et des styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **PUSHBUTTON** :

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Boutons de commande](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 