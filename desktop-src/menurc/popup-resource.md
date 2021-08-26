---
title: Ressource contextuelle
description: Définit un élément de menu qui peut contenir des éléments de menu et des sous-menus.
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- Menus contextuels de ressources et autres ressources
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f134b2d5801bc5003be6f45b42d13f1668c2e684b5f63fe0aed1f2c9c0400860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952339"
---
# <a name="popup-resource"></a>Ressource contextuelle

Définit un élément de menu qui peut contenir des éléments de menu et des sous-menus.

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Chaîne qui contient le nom du menu. Cette chaîne doit être placée entre guillemets doubles (**"**).

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Ce paramètre spécifie les options de menu redéfinies qui spécifient l’apparence de l’élément de menu. Ce paramètre facultatif peut être un ou plusieurs des éléments suivants.



| Option           | Description                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DÉSACTIVÉ**      | L’élément de menu est coché. Cette option n’est pas valide pour un menu de niveau supérieur.                                                                                 |
| **GRISÉ**       | L’élément de menu est initialement inactif et apparaît dans le menu en gris ou une nuance éclaircie de la couleur de texte de menu. Cette option ne peut pas être utilisée avec l’option **inactive** . |
| **AIDE**         | Identifie un élément d’aide. L’élément de menu est placé à la position la plus à droite dans la barre de menus.                                                                            |
| **INACTIVE**     | L’élément de menu est affiché, mais il ne peut pas être sélectionné. Cette option ne peut pas être utilisée avec l’option **grisé** .                                                              |
| **MENUBARBREAK** | Identique à **MENUBREAK** , sauf que pour les menus contextuels, il sépare la nouvelle colonne de l’ancienne colonne par une ligne verticale.                                             |
| **MENUBREAK**    | Place l’élément de menu sur une nouvelle ligne pour les éléments de barre de menus statiques. Pour les menus, il place l’élément de menu dans une nouvelle colonne sans ligne de séparation entre les colonnes.           |



 

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **Popup** :

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**MENUITEM**](menuitem-statement.md)
</dt> </dl>

 

 




