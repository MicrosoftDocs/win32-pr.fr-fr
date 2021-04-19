---
title: Contrôle DEFPUSHBUTTON
description: Définit un contrôle de bouton de commande par défaut.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menus du contrôle DEFPUSHBUTTON et autres ressources
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106543614"
---
# <a name="defpushbutton-control"></a>Contrôle DEFPUSHBUTTON

Définit un contrôle de bouton de commande par défaut. Le contrôle est un petit rectangle avec un plan en gras qui représente la réponse par défaut pour l’utilisateur. Le texte indiqué s’affiche à l’intérieur du bouton. Le contrôle met en surbrillance le bouton de la manière habituelle lorsque l’utilisateur clique sur la souris et envoie un message à sa fenêtre parente.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Texte à centrer dans la zone rectangulaire du contrôle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison des styles suivants : **BS \_ DEFPUSHBUTTON**, **WS \_ TABSTOP**, **WS \_ Group** et **WS \_ Disabled**.

Si vous ne spécifiez pas de style, le style par défaut est `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de bouton de commande par défaut intitulé Cancel :

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Boutons de commande](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**BOUTONS**](pushbutton-control.md)
</dt> <dt>

[**Button**](radiobutton-control.md)
</dt> </dl>

 

 




