---
title: Contrôle COMBOBOX (menus et autres ressources)
description: Définit un contrôle de zone combinée (une zone de liste déroulante).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menus du contrôle COMBOBOX et autres ressources
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2ffaa64266d9b370cca5215725eb45d0f620054c66562e3f60492441e38890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972118"
---
# <a name="combobox-control"></a>COMBOBOX, contrôle

Définit un contrôle de zone combinée (une zone de liste déroulante). Une zone de liste déroulante est constituée d’une zone de texte statique ou d’une zone d’édition associée à une zone de liste. La zone de liste peut être affichée à tout moment ou extraite par l’utilisateur. Si la zone de liste déroulante contient une zone de texte statique, la zone de texte affiche toujours la sélection (le cas échéant) dans la partie de la zone de liste de la zone de liste déroulante. Si elle utilise une zone d’édition, l’utilisateur peut taper la sélection souhaitée ; la zone de liste met en surbrillance le premier élément (le cas échéant) qui correspond à ce que l’utilisateur a entré dans la zone d’édition. L’utilisateur peut ensuite sélectionner l’élément mis en surbrillance dans la zone de liste pour terminer le choix. En outre, la zone de liste déroulante peut être owner-drawn et de hauteur fixe ou variable.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison des styles de la classe COMBOBOX et de l’un des styles suivants : **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** et **WS \_ désactivé**.

Si vous ne spécifiez pas de style, le style par défaut est `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

Le paramètre *Height* s’applique à la hauteur d’une zone de liste déroulante avec une liste déroulante entièrement développée.

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de zone de liste déroulante avec une barre de défilement verticale :

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Zones de liste modifiable](../controls/about-combo-boxes.md)
</dt> </dl>

 

 