---
title: Annotation de la carte des valeurs
description: Annotation de la carte des valeurs
ms.assetid: f7c9304a-0eed-4a73-ab06-56723f3cfa5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d21b04374344475689989c2570af6975dc97c13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104552144"
---
# <a name="value-map-annotation"></a>Annotation de la carte des valeurs

Avec l’annotation de mappage de valeur, vous pouvez utiliser une chaîne de mappage pour indiquer la façon dont l’index d’image d’un élément d’un affichage de liste ou d’une arborescence correspond à son rôle ou état. Par exemple, une chaîne de mappage peut indiquer que l’index d’images d’un affichage de liste est mappé à un rôle de case à cocher, tandis que l’index d’image 1 est mappé à un rôle de case d’option.

Vous pouvez également utiliser l’annotation de mappage de valeur pour spécifier des chaînes qui mappent aux valeurs numériques sur un curseur.

## <a name="when-to-use-this-technique"></a>Quand utiliser cette technique

Envisagez d’utiliser l’annotation de mappage de valeur dans les cas suivants.

-   Lorsqu’une vue de liste ou une arborescence owner-drawn incorpore l’utilisation d’images, et que vous souhaitez fournir une description accessible personnalisée (propriété [**Description**](description-property.md) ) en fonction de cette image. L'illustration suivante montre un exemple.

    ![illustration du menu Démarrer, où les icônes fournissent des indications visuelles sur le contenu](images/iconlist.gif)

-   Lorsqu’un contrôle d’affichage de liste ou d’arborescence owner-drawn incorpore l’utilisation d’images pour que les éléments d’arborescence ou de liste agissent comme des contrôles simples, généralement des cases à cocher ou des cases d’option, et que vous souhaitez mapper l’image à un rôle. La capture d’écran suivante montre un exemple.

    ![capture d’écran des options d’Internet Explorer pour définir la valeur des cases à cocher et des cases d’option](images/customlist.gif)

-   Lorsqu’un curseur est utilisé pour sélectionner une valeur qui peut être décrite comme autre chose qu’un simple entier, comme dans la capture d’écran suivante, où le paramètre de résolution d’écran est décrit par une chaîne.

    ![capture d’écran d’un curseur utilisé pour définir la résolution de l’écran](images/slider.gif)

Avec l’annotation de mappage de valeur, une chaîne de mappage indique comment l’index d’image de la liste ou de l’arborescence correspond à son rôle ou état. Ou, il peut indiquer comment la valeur numérique d’un curseur correspond à une chaîne. Par exemple, une chaîne de mappage peut indiquer que l’index d’image d’une vue Liste 0 correspond à un rôle de case à cocher et que l’index d’image 1 est mappé à un rôle de case d’option. Utilisez [**IAccPropServices :: SetHwndPropStr ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) pour attacher la chaîne de mappage au contrôle.

Étant donné que les connaissances spécifiques aux contrôles sont requises pour prendre en charge le mappage de valeur, il existe un nombre limité de contrôles et de propriétés qui prennent en charge l’annotation de correspondance de valeur, y compris les mappages de valeur de curseur, les vues de liste et les arborescences.

## <a name="slider-value-map"></a>Mappage des valeurs du curseur

**Propid \_ Le compte \_ VALUEMAP VALUEMAP** contient une correspondance entre les positions de curseur internes et les chaînes explicites. Cette propriété est prise en charge par le proxy Oleacc.dll Slider. Si la valeur de curseur actuelle est trouvée dans le mappage des valeurs, la chaîne correspondante sera exposée en tant que valeur au lieu de la chaîne de pourcentage par défaut (par exemple, « 50 »).

## <a name="list-view-and-tree-view"></a>Mode liste et arborescence

**Propid \_ ACC \_ ROLEMAP**, **propid \_ ACC \_ STATEMAP** et **propid \_ ACC \_ DESCRIPTONMAP** fournissent des mappages des index d’images d’État aux valeurs de rôle et d’État. Ces mappages permettent aux index d’images d’être mappés aux rôles appropriés (généralement, les contrôleurs de contrôle de système de [**rôle \_ \_**](object-roles.md) ou les [**CHECKBUTTON de \_ système \_ de rôle**](object-roles.md)) et les bits d’État supplémentaires (en général, le [**système d’État est \_ \_ activé**](object-state-constants.md)).

Pour plus d’informations sur les annotations de mappage des valeurs, consultez les rubriques suivantes :

-   [Utilisation de l’annotation de mappage de valeur](using-value-map-annotation.md)
-   [Exemple d’annotation Map value](value-map-annotation-sample.md)

## <a name="annotation-map-format"></a>Format de la carte des annotations

Le tableau suivant décrit les champs inclus dans une carte d’annotation.



| Champ               | Description                                                                                                                                                                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Un                 | Indique qu’un schéma de codage particulier est utilisé. Des préfixes supplémentaires peuvent être pris en charge pour les futurs schémas d’encodage.                                                                                                                                                          |
| Caractère délimiteur | Généralement un signe deux-points ( :) est utilisé, mais il peut s’agir d’un autre caractère, à l’exception de **null** ou d’un espace vide. Étant donné que ce caractère sera utilisé comme délimiteur pour les champs restants, il ne peut pas être utilisé dans le cadre d’une valeur de la carte.                                               |
| 0, 1 ou 2          | Valeur qui indique quelle clé est utilisée. Pour le rôle d’arborescence et d’affichage de liste et les mappages d’État, cette clé peut avoir la valeur 0 (index d’images), 1 (index d’images d’État) ou 2 (index d’images de superposition). Pour les curseurs et autres contrôles qui n’offrent pas de choix de clés, cette valeur doit être 0. |
| Caractère délimiteur | :                                                                                                                                                                                                                                                                             |
| Paires clé-valeur     | Chaque paire se compose d’une chaîne de clé et d’un caractère délimiteur. La chaîne de clé est un nombre et peut être au format décimal ou hexadécimal (avec un préfixe « 0x » de début).                                                                                                            |
| Chaîne de valeur        | Pour les mappages de valeurs, il s’agit d’une chaîne. Pour les mappages de rôles et d’États, il s’agit d’un nombre (décimal ou hexadécimal).                                                                                                                                                                         |
| Caractère délimiteur | :                                                                                                                                                                                                                                                                             |



 

Par exemple, une carte peut se présenter comme suit :


```C++
A:0:0:Cold:1:Warm:3:Hot:
```



Lorsque cette carte de valeur est appliquée à un contrôle Slider, la valeur « chaude » est exposée lorsque le curseur se trouve à la position 1. Étant donné que la valeur 2 n’est pas incluse dans cet exemple, la valeur par défaut de cette position sera exposée. Pour un curseur, la valeur par défaut est une valeur en pourcentage, telle que 33.

 

 




