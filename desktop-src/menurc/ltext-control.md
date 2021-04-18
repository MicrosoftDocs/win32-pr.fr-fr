---
title: Contrôle LTEXT
description: Définit un contrôle de texte aligné à gauche.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menus du contrôle LTEXT et autres ressources
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509253"
---
# <a name="ltext-control"></a>Contrôle LTEXT

Définit un contrôle de texte aligné à gauche. Le contrôle est un rectangle simple qui affiche le texte spécifié à gauche dans le rectangle. Le texte est mis en forme avant d’être affiché. Les mots qui s’étendent au-delà de la fin d’une ligne sont automatiquement renvoyés au début de la ligne suivante. Les mots qui sont plus longs que la largeur du contrôle sont tronqués.

L’instruction **LTEXT** , qui peut être utilisée uniquement dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs du contrôle.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être n’importe quelle combinaison du style **\_ RadioButton BS** et des styles suivants : **SS \_ Left**, **WS \_ TABSTOP** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `SS_LEFT | WS_GROUP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de texte aligné à gauche nommé filename :

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RÉGULATION**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Contrôles d’édition](../controls/about-edit-controls.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 