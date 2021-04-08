---
description: Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034931"
---
# <a name="include-element"></a>include, élément

Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.

## <a name="usage"></a>Utilisation

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
| [**fichier**](file.md)<br/> | Indique au générateur de code de générer un fichier et spécifie le nom du fichier de sortie.<br/> <br/> |



## <a name="remarks"></a>Notes

L’attribut de **macro** ou l’attribut de **fichier** doit être spécifié. Ne spécifiez pas les deux attributs.

WsdCodeGen définit une macro nommée **DoNotModify**. Lorsque cette macro est incluse, le code généré contient un bloc de commentaires de visibilité élevée qui indique aux développeurs qu’ils ne peuvent pas modifier le code généré.

## <a name="examples"></a>Exemples

Le code XML suivant montre comment inclure la macro **DoNotModify** . Ce code XML peut être ajouté à un fichier de configuration XML pour WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




