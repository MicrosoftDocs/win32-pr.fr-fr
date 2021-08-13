---
title: Contrôle AUTO3STATE
description: Définit une case à cocher à trois États automatique.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menus du contrôle AUTO3STATE et autres ressources
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318d43f0b6d8a16d6e76ae3d12f934e41e265197690a955cfe148dd71176f440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735211"
---
# <a name="auto3state-control"></a>Contrôle AUTO3STATE

Définit une case à cocher à trois États automatique. Le contrôle est une zone ouverte avec le texte spécifié placé à droite de la zone. Lorsque vous choisissez cette option, la zone passe automatiquement d’un État à l’autre : activée, désactivée et désactivée (grisée). Le contrôle envoie un message à son parent chaque fois que l’utilisateur choisit le contrôle.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles pour le contrôle, qui peut être une combinaison du style **BS \_ AUTO3STATE** et des styles suivants : **WS \_ TABSTOP**, **WS \_ Disabled** et **WS \_ Group**.

Si vous ne spécifiez pas de style, le style par défaut est `BS_AUTO3STATE | WS_TABSTOP` .

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
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Styles de fenêtre](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 