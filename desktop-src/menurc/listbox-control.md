---
title: LISTBOX, contrôle (menus et autres ressources)
description: Définit les contrôles couramment utilisés pour une boîte de dialogue ou une fenêtre. Le contrôle est un rectangle qui contient une liste de chaînes (telles que des noms de fichiers) à partir desquelles l’utilisateur peut sélectionner.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menus du contrôle LISTBOX et autres ressources
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101608"
---
# <a name="listbox-control"></a>LISTBOX, contrôle

Définit les contrôles couramment utilisés pour une boîte de dialogue ou une fenêtre. Le contrôle est un rectangle qui contient une liste de chaînes (telles que des noms de fichiers) à partir desquelles l’utilisateur peut sélectionner.

L’instruction **ListBox** , qui peut uniquement être utilisée dans une instruction [**DIALOGEX**](dialogex-resource.md) ou **Window** , définit l’identificateur, les dimensions et les attributs d’une fenêtre de contrôle.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Cette valeur peut être une combinaison des styles de classe de zone de liste et de l’un des styles suivants : **WS \_ Border** et **WS \_ VSCROLL**.

Si vous ne spécifiez pas de style, le style par défaut est `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md).

## <a name="examples"></a>Exemples

Cet exemple définit un contrôle de zone de liste dont l’identificateur est 101 :

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**COMBOBOX**](combobox-control.md)
</dt> <dt>

[Zones de liste](../controls/about-list-boxes.md)
</dt> </dl>

 

 