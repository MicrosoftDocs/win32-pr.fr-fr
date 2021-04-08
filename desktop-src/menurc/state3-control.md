---
title: Contrôle STATE3
description: Définit un contrôle de case à cocher à trois États. Le contrôle est identique à une case à cocher, à la différence qu’il a trois États activés, désactivés et désactivés (en grisé).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menus du contrôle STATE3 et autres ressources
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678286"
---
# <a name="state3-control"></a>Contrôle STATE3

Définit un contrôle de case à cocher à trois États. Le contrôle est identique à une [**case à cocher**](checkbox-control.md), à la différence qu’il a trois États : activé, désactivé et désactivé (grisé).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Texte à afficher à droite du contrôle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison du style de classe Button **BS \_ 3STATE** et des styles **WS \_ TABSTOP** et **WS \_ Group** .

Si vous ne spécifiez pas de style, le style par défaut est `BS_3STATE | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CASE d’option**](autocheckbox-control.md)
</dt> <dt>

[Cases à cocher](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**ACTIVÉ**](checkbox-control.md)
</dt> <dt>

[**RÉGULATION**](control-control.md)
</dt> </dl>

 

 




