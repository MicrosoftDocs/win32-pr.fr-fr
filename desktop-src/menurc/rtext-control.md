---
title: Contrôle RTEXT
description: Définit un contrôle de texte aligné à droite.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menus du contrôle RTEXT et autres ressources
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463134"
---
# <a name="rtext-control"></a>Contrôle RTEXT

Définit un contrôle de texte aligné à droite. Le contrôle est un rectangle simple qui affiche le texte donné aligné à droite dans le rectangle. Le texte est mis en forme avant d’être affiché. Les mots qui s’étendent au-delà de la fin d’une ligne sont automatiquement renvoyés au début de la ligne suivante. Les mots qui sont plus longs que la largeur du contrôle sont tronqués.

L’instruction **rtext** , qui peut être utilisée uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs du contrôle.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles pour le contrôle de texte, qui peut être n’importe quelle combinaison des éléments suivants : **WS \_ TABSTOP** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **rtext** :

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RÉGULATION**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Contrôles d’édition](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 