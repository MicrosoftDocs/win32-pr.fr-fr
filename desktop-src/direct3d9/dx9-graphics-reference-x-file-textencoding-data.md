---
description: Les objets de données contiennent les données réelles ou une référence à ces données. Chaque objet de données a un modèle correspondant qui spécifie le type de données. Les sections suivantes décrivent le formulaire et les parties des objets de données.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Données (format de fichier X, encodage de texte)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acd4222e2878b882b8777e3ba22e28f2d213fb5f3550686baf29b4ed6719e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730200"
---
# <a name="data-x-file-format-text-encoding"></a>Données (format de fichier X, encodage de texte)

Les objets de données contiennent les données réelles ou une référence à ces données. Chaque objet de données a un modèle correspondant qui spécifie le type de données. Les sections suivantes décrivent le formulaire et les parties des objets de données.

## <a name="form-identifier-and-name"></a>Formulaire, identificateur et nom

Les objets de données se présentent sous la forme suivante.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



L’identificateur est obligatoire et doit correspondre à un type de données ou une primitive défini précédemment. Toutefois, le nom est facultatif.

## <a name="data-members"></a>Données membres

Les membres de données peuvent être l’un des suivants : objet de données, référence de données, liste d’entiers, liste flottante ou liste de chaînes.

Un objet de données est un objet de données imbriqué. Cela permet d’exprimer la nature hiérarchique du format de fichier. Les types d’objets de données imbriquées autorisés dans la hiérarchie peuvent être restreints.

Une référence de données est une référence à un objet de données précédemment rencontré, comme illustré dans l’exemple suivant.


```
{
  name |
  UUID |
  name UUID
}
```



Une liste d’entiers est une liste d’entiers séparés par des points-virgules, comme illustré dans l’exemple suivant.


```
1; 2; 3;
```



Une liste flottante est une liste de valeurs float séparées par des points-virgules, comme illustré dans l’exemple suivant.


```
1.0; 2.0; 3.0;
```



Une liste de chaînes est une liste de chaînes séparées par des points-virgules, comme illustré dans l’exemple suivant.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage de texte](text-encoding.md)
</dt> </dl>

 

 



