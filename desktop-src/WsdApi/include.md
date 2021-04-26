---
description: Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995776"
---
# <a name="include-element"></a>include, élément

Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.

## <a name="usage"></a>Usage

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a>Attributs



| Attribut            | Type                         | Obligatoire      | Description                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **file**<br/>  | chaîne de caractères \_<br/> | Non<br/> | Chemin d’accès au fichier à inclure.<br/> <br/>  |
| **macrovirus**<br/> | chaîne de caractères \_<br/> | Non<br/> | Nom de la macro à inclure.<br/> <br/> |



## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                         | Description                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**txt**](file.md)<br/> | Indique au générateur de code de générer un fichier et spécifie le nom du fichier de sortie.<br/> <br/> |



## <a name="remarks"></a>Remarques

L’attribut de **macro** ou l’attribut de **fichier** doit être spécifié. Ne spécifiez pas les deux attributs.

WsdCodeGen définit une macro nommée **DoNotModify**. Lorsque cette macro est incluse, le code généré contient un bloc de commentaires de visibilité élevée qui indique aux développeurs qu’ils ne peuvent pas modifier le code généré.

## <a name="examples"></a>Exemples

Le code XML suivant montre comment inclure la macro **DoNotModify** . Ce code XML peut être ajouté à un fichier de configuration XML pour WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




