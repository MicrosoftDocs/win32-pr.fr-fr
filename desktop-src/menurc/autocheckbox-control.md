---
title: Contrôle de case à cocher
description: Définit un contrôle de case à cocher automatique.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menus du contrôle de case à cocher et autres ressources
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725557"
---
# <a name="autocheckbox-control"></a>Contrôle de case à cocher

Définit un contrôle de case à cocher automatique. Le contrôle est un petit rectangle (case à cocher) auquel le texte spécifié est affiché en regard de celui-ci (généralement, à droite). Quand l’utilisateur choisit le contrôle, le contrôle met en surbrillance le rectangle et envoie un message à sa fenêtre parente.

L’instruction **autocase** ne peut être utilisée que dans le corps d’une instruction [**Dialog**](dialog-resource.md) ou [**DIALOGEX**](dialogex-resource.md) .

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles du contrôle. Cette valeur peut être une combinaison du style de classe de bouton **BS \_ autocase** et des styles **WS \_ TABSTOP** et **WS \_ Group** .

Si vous ne spécifiez pas de style, le style par défaut est `BS_AUTOCHECKBOX | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Styles de bouton](../controls/button-styles.md)
</dt> <dt>

[**ACTIVÉ**](checkbox-control.md)
</dt> <dt>

[**RÉGULATION**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 