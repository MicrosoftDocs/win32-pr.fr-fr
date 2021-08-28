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
ms.openlocfilehash: 24db89c986f3f6d466f1710bc18420f9da9eec3348eada10e95582a882fe25e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776999"
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

 

 