---
title: MENUITEM (instruction)
description: Définit un élément de menu.
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- Menus d’instructions MENUITEM et autres ressources
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bca50025e1c9136c22166d6d3f758c5c9b5819a9328d33d375195285f1d4f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092189"
---
# <a name="menuitem-statement"></a>MENUITEM (instruction)

Définit un élément de menu.

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Nom de l'élément de menu.

La chaîne peut contenir les caractères d’échappement **\\ t** et **\\ a**. Le caractère **\\ t** insère un onglet dans la chaîne et est utilisé pour aligner le texte dans les colonnes. Les caractères de tabulation doivent être utilisés uniquement dans les menus, pas dans les barres de menus. (Pour plus d’informations sur les menus, consultez la rubrique de la [**ressource contextuelle**](popup-resource.md).) Le caractère **\\ a** aligne tout le texte qui suit son vidage directement dans la barre de menus ou le menu contextuel.

</dd> <dt>

<span id="result"></span><span id="RESULT"></span>*venir*
</dt> <dd>

Nombre qui spécifie le résultat généré lorsque l’utilisateur sélectionne l’élément de menu. Ce paramètre prend une valeur entière. Les résultats de l’élément de menu sont toujours des entiers ; Quand l’utilisateur clique sur le nom de l’élément de menu, le résultat est envoyé à la fenêtre qui possède le menu.

</dd> <dt>

<span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*
</dt> <dd>

Apparence de l’élément de menu. Ce paramètre facultatif prend une ou plusieurs des options de menu redéfinies suivantes, séparées par des virgules ou des espaces.



| Option           | Description                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DÉSACTIVÉ**      | L’élément de menu est coché.                                                                                                                                |
| **GRISÉ**       | L’élément de menu est initialement inactif et apparaît dans le menu en gris ou une nuance éclaircie de la couleur de texte de menu. Cette option ne peut pas être utilisée avec l’option **inactive** . |
| **AIDE**         | Identifie un élément d’aide. Cette option n’a aucun effet sur l’apparence de l’élément de menu.                                                                                 |
| **INACTIVE**     | L’élément de menu est affiché, mais il ne peut pas être sélectionné. Cette option ne peut pas être utilisée avec l’option **grisé** .                                                              |
| **MENUBARBREAK** | Identique à **MENUBREAK** , sauf que pour les menus contextuels, il sépare la nouvelle colonne de l’ancienne colonne par une ligne verticale.                                             |
| **MENUBREAK**    | Place l’élément de menu sur une nouvelle ligne pour les éléments de barre de menus statiques. Pour les menus, il place l’élément de menu dans une nouvelle colonne sans ligne de séparation entre les colonnes.           |



 

</dd> <dt>

<span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM, SÉPARATEUR**
</dt> <dd>

Le formulaire de **séparateur MenuItem** de l’instruction **MenuItem** crée un élément de menu inactif qui sert de barre de séparation entre deux éléments de menu actifs d’un menu.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation des instructions de séparateur **MenuItem** et **MenuItem** :

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MENUS**](menu-resource.md)
</dt> <dt>

[**MESSAGES**](popup-resource.md)
</dt> </dl>

 

 




