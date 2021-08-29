---
title: Ressource de MENU
description: Définit le contenu d’une ressource de menu. | Ressource de MENU
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menus de ressources de MENU et autres ressources
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2b73afb5ef0547cbbccd8e5fdd87d7581edcaf19d5d73bc49ea3151166d882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601939"
---
# <a name="menu-resource"></a>Ressource de MENU

Définit le contenu d’une ressource de menu. Une ressource de menu est un ensemble d’informations qui définit l’apparence et la fonction d’un menu d’application. Un menu est un outil d’entrée spécial qui permet à un utilisateur de sélectionner des commandes et d’ouvrir des sous-menus dans une liste d’éléments de menu.

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*
</dt> <dd>

Numéro qui identifie le menu. Cette valeur est soit une chaîne unique, soit une valeur d’entier 16 bits non signé unique comprise entre 1 et 65 535.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instructions facultatives*
</dt> <dd>

Ce paramètre peut avoir une valeur égale à zéro parmi les instructions suivantes.



| .                                                        | Description                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caractéristiques**](characteristics-statement.md) *DWORD*     | Informations définies par l’utilisateur sur une ressource qui peuvent être utilisées par des outils qui lisent et écrivent des fichiers de ressources. Pour plus d’informations, consultez [**caractéristiques**](characteristics-statement.md). |
| [](language-statement.md) *Langue* langue, sous- *langue* | Langue de la ressource. Pour plus d’informations, consultez [**Language**](language-statement.md).                                                                                            |
| [**Version**](version-statement.md) *DWORD*                     | Numéro de version défini par l’utilisateur pour la ressource qui peut être utilisé par les outils qui lisent et écrivent les fichiers de ressources. Pour plus d’informations, consultez [**version**](version-statement.md).              |



 

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="examples"></a>Exemples

Voici un exemple d’instruction de **menu** complète :

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des menus](./using-menus.md)
</dt> <dt>

[**ACCÉLÉRATEURS**](accelerators-resource.md)
</dt> <dt>

[**ATTRIBUTS**](characteristics-statement.md)
</dt> <dt>

[**SOUS**](language-statement.md)
</dt> <dt>

[**MENUEX**](menuex-resource.md)
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

 

 
