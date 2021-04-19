---
description: Décrit un espace de noms.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380843"
---
# <a name="namespace-element"></a>nameSpace, élément

Décrit un espace de noms. Cet espace de noms peut être utilisé pour la génération de code ou pour la gestion de \<wsdl:import> directives.

## <a name="usage"></a>Usage

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>Attributs



| Attribut          | Type                         | Obligatoire       | Description                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **uri**<br/> | chaîne de caractères \_<br/> | Oui<br/> | URI unique de l’espace de noms.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                               | Description                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Baptisé**](codename.md)<br/>               | Nom à utiliser pour identifier l’espace de noms dans le code généré.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | Préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.<br/> <br/> |
| [**nomme**](name.md)<br/>                       | Nom qualifié dans l’espace de noms.<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | Préfixe auquel l’espace de noms doit être mappé pour rendre le XML plus lisible.<br/> <br/> |



### <a name="child-element-sequence"></a>Séquence d’éléments enfants

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a>Éléments parents



| Élément                                     | Description                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Élément racine d’un fichier de script XML du générateur de code WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet élément peut être utilisé pour fournir le générateur de code avec des informations supplémentaires sur les espaces de noms qu’il rencontre dans les fichiers WSDL et XSD ou pour introduire de nouveaux espaces de noms.

Les espaces de noms implicites par la réflexion de type ou spécifiés dans les fichiers WSDL et XSD sont analysés automatiquement par le générateur de code et n’ont pas besoin d’être explicitement définis dans le script. Dans certains cas, cet élément peut être utilisé pour ajouter des propriétés ou des noms supplémentaires à un espace de noms référencé par la réflexion de type ou WSDL/XSD. Le générateur de code ne considère pas ceci comme un conflit.

Le code XML suivant montre un élément d’espace de noms (avec des enfants omis par souci de concision).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




