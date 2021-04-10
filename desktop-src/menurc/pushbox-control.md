---
title: Contrôle PUSHBOX
description: Définit un contrôle de zone de notification, qui est identique à un bouton de commande, à ceci près qu’il n’affiche pas de visage ou de cadre de bouton. seul le texte s’affiche.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Menus du contrôle PUSHBOX et autres ressources
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3e81e11c7d9a87c4f5501b114ef77cdb88b07
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100921"
---
# <a name="pushbox-control"></a>Contrôle PUSHBOX

Définit un contrôle de zone de notification, qui est identique à [**un bouton de commande**](pushbutton-control.md), à ceci près qu’il n’affiche pas de visage ou de cadre de bouton. seul le texte s’affiche.

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles pour PUSHBOX, qui peut être une combinaison du style **BS \_ PUSHBOX** et des styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `BS_PUSHBOX | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Boutons de commande](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**BOUTONS**](pushbutton-control.md)
</dt> </dl>

 

 




