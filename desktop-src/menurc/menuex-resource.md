---
title: Ressource MENUEX
description: Définit le contenu d’une ressource de menu. | Ressource MENUEX
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- Menus de ressources MENUEX et autres ressources
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec78bd0d33b48b11de77fe7742affb4265160752ffad30d72ecf3e9c173bb77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825939"
---
# <a name="menuex-resource"></a>Ressource MENUEX

Définit le contenu d’une ressource de menu. Une ressource de menu est un ensemble d’informations qui définit l’apparence et la fonction d’un menu d’application. Un menu est un outil d’entrée spécial qui permet à un utilisateur de sélectionner des commandes et d’ouvrir des sous-menus dans une liste d’éléments de menu. Il définit également les éléments suivants :

-   Identificateurs d’aide dans les menus.
-   Identificateurs dans les menus.
-   Utilisation des indicateurs de type **MFT \_ \** _ et des indicateurs d’état _*MFS \_ \**_ . Pour plus d’informations sur ces indicateurs, consultez la structure [_ *MENUITEMINFO* *](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) .

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)
</dt> <dd>

Définit un élément de menu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Chaîne contenant le texte de l’élément de menu. Pour plus d’informations, consultez [**MenuItem**](menuitem-statement.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Expression numérique indiquant l’identificateur de l’élément de menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*entrer*
</dt> <dd>

Expression numérique indiquant le type de l’élément de menu utilisé pour les valeurs de type MFT prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Département*
</dt> <dd>

Expression numérique indiquant l’état de l’élément de menu pour utiliser les valeurs d’État MFS prédéfinies \_ \* , incluez l’instruction suivante dans votre. Fichier RC :`#include "winuser.h"`

</dd> </dl> </dd> <dt>

<span id="POPUP"></span><span id="popup"></span>[**MESSAGES**](popup-resource.md)
</dt> <dd>

Définit un élément de menu associé à un sous-menu.

<dl> <dt>

<span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*
</dt> <dd>

Chaîne contenant le texte de l’élément de menu.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Expression numérique indiquant l’identificateur de l’élément de menu.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*entrer*
</dt> <dd>

Expression numérique indiquant le type de l’élément de menu utilisé pour les valeurs de type MFT prédéfinies \_ \* , incluez l’instruction suivante dans votre. Fichier RC :`#include "winuser.h"`

</dd> <dt>

<span id="state"></span><span id="STATE"></span>*Département*
</dt> <dd>

Expression numérique indiquant l’état de l’élément de menu pour utiliser les valeurs d’État MFS prédéfinies \_ \* , incluez l’instruction suivante dans votre fichier. RC :`#include "winuser.h"`

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*
</dt> <dd>

Expression numérique indiquant l’identificateur utilisé pour identifier le menu lors du traitement de [**\_ l’aide WM**](../shell/wm-help.md) .

</dd> </dl> </dd> <dt>

<span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*
</dt> <dd>

Contient toute combinaison d’instructions [**MenuItem**](menuitem-statement.md) et [**Popup**](popup-resource.md) .

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="remarks"></a>Remarques

Les opérations arithmétiques et booléennes valides qui peuvent être contenues dans les expressions numériques des instructions de **menuex** sont les suivantes :

-   Add (' + ')
-   Soustraire ('-')
-   Moins unaire ('-')
-   NOT unaire (' ~ ')
-   AND (' & ')
-   OU (' \| ')

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des menus](./using-menus.md)
</dt> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**DIALOGUE**](dialog-resource.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> <dt>

[**MESSAGES**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSION**](version-statement.md)
</dt> </dl>

 

 
