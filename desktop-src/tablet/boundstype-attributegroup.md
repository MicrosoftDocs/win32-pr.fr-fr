---
description: Définit un groupe d’attributs utilisé par divers éléments dans un fichier journal XML. Elle contient des attributs utilisés pour définir les limites (gauche, haut, hauteur et largeur) d’un élément dans le document.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Groupe d’attributs BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba91269660875e55b92797609969ebee38d221016914d9473cd5eddd245cfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967768"
---
# <a name="boundstype-attribute-group"></a>Groupe d’attributs BoundsType

Définit un groupe d’attributs utilisé par divers éléments dans un fichier journal XML. Elle contient des attributs utilisés pour définir les limites (gauche, haut, hauteur et largeur) d’un élément dans le document.

## <a name="definition"></a>Définition

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a>Éléments enfants

Aucun.

## <a name="attributes"></a>Attributs



| Attribut  | Type                      | Obligatoire | Description                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.<br/> | N’importe quel entier.<br/>              |
| **Top**    | **xs:integer**            | Obligatoire | Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.<br/>  | N’importe quel entier.<br/>              |
| **Width**  | **xs:nonNegativeInteger** | Obligatoire | Largeur de la zone englobante pour l’élément.<br/>                                          | Entier non négatif.<br/> |
| **Height** | **xs:nonNegativeInteger** | Obligatoire | Hauteur du rectangle englobant pour l’élément.<br/>                                         | Entier non négatif.<br/> |



 

## <a name="type-information"></a>Informations de type



|                 | Valeur                                      |
|-----------------|--------------------------------------------|
| **Espace de noms**   | urn : schemas-microsoft-com : TabletPC : RichInk |
| **Nom du schéma** | Lecteur de journal                             |



 

## <a name="remarks"></a>Remarques

**Left** et **Top** peuvent être négatifs, car l’origine est définie par les marges, et non par la page.

 

 




