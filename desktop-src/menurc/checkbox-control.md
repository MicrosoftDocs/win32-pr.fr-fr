---
title: CHECKBOX, contrôle (compilateur de ressources)
description: Définit un contrôle de case à cocher.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menus du contrôle CHECKBOX et autres ressources
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461329"
---
# <a name="checkbox-control"></a>CHECKBOX (contrôle)

Définit un contrôle de case à cocher. Le contrôle est un petit rectangle (case à cocher) auquel le texte spécifié est affiché en regard de celui-ci (généralement, à droite). Lorsque l’utilisateur sélectionne le contrôle, le contrôle met en surbrillance le rectangle et envoie un message à sa fenêtre parente.

L’instruction **CheckBox** , qui peut uniquement être utilisée dans une instruction [**DIALOGEX**](dialogex-resource.md) , définit le texte, l’identificateur, les dimensions et les attributs du contrôle.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Texte à afficher à droite du contrôle.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison de la **\_ case à cocher** de style de classe de bouton BS et des styles **WS \_ TABSTOP** et **WS \_ Group** .

Si vous ne spécifiez pas de style, le style par défaut est `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de case à cocher intitulé italique :

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CASE d’option**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Cases à cocher](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 