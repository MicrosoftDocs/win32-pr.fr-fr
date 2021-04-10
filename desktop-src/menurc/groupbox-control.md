---
title: GROUPBOX, contrôle (menus et autres ressources)
description: Définit un contrôle de zone de groupe. Le contrôle est un rectangle qui regroupe d’autres contrôles. Les contrôles sont regroupés en dessinant une bordure autour et en affichant le texte indiqué dans le coin supérieur gauche.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menus du contrôle GROUPBOX et autres ressources
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104030549"
---
# <a name="groupbox-control"></a>GROUPBOX, contrôle

Définit un contrôle de zone de groupe. Le contrôle est un rectangle qui regroupe d’autres contrôles. Les contrôles sont regroupés en dessinant une bordure autour et en affichant le texte indiqué dans le coin supérieur gauche.

L’instruction **GroupBox** , que vous pouvez utiliser uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs d’une fenêtre de contrôle.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison de la zone de style de classe de bouton **BS \_ GroupBox** et des styles **WS \_ TABSTOP** et **WS \_ Disabled** .

Si vous ne spécifiez pas de style, le style par défaut est **BS \_ GroupBox**.

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="remarks"></a>Notes

Quand le style contient **WS \_ TABSTOP** ou que le texte spécifie un accélérateur, la tabulation ou la touche d’accès rapide déplace le focus sur le premier contrôle au sein du groupe.

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de zone de groupe qui est étiqueté options :

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Zones de groupe](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




