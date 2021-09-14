---
title: Contrôle CTEXT
description: Définit un contrôle de texte centré.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menus du contrôle CTEXT et autres ressources
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196743"
---
# <a name="ctext-control"></a>Contrôle CTEXT

Définit un contrôle de texte centré. Le contrôle est un rectangle simple qui affiche le texte donné centré dans le rectangle. Le texte est mis en forme avant d’être affiché. Les mots qui s’étendent au-delà de la fin d’une ligne sont automatiquement renvoyés au début de la ligne suivante. Les mots qui sont plus longs que la largeur du contrôle sont tronqués.

L’instruction [**LTEXT**](ltext-control.md) , qui peut être utilisée uniquement dans une instruction REP, définit le texte, l’identificateur, les dimensions et les attributs du contrôle.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Texte à centrer dans la zone rectangulaire du contrôle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être n’importe quelle combinaison des styles suivants : **SS \_ Center**, **WS \_ TABSTOP** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `SS_CENTER | WS_GROUP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de texte centré intitulé filename :

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RÉGULATION**](control-control.md)
</dt> <dt>

[Contrôles d’édition](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 