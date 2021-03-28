---
description: Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément. Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Comment utiliser le modèle de sélection de verbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973159"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Comment utiliser le modèle de sélection de verbe

Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément. Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe.

## <a name="instructions"></a>Instructions


Spécifiez la valeur MultiSelectModel pour tous les verbes. Si la valeur MultiSelectModel n’est pas spécifiée, elle est déduite du type d’implémentation de verbe que vous avez choisi. Pour les méthodes basées sur COM (par exemple, DropTarget et ExecuteCommand), le **lecteur** est supposé, et pour les autres méthodes, le **document** est supposé.

Les valeurs possibles pour le modèle de sélection de verbe sont les suivantes :

1.  Spécifiez **Single** pour les verbes qui prennent en charge une seule sélection.
2.  Spécifiez **Player** pour les verbes qui prennent en charge un nombre quelconque d’éléments.
3.  Spécifiez **document** pour les verbes qui créent une fenêtre de niveau supérieur pour chaque élément. Cela limite le nombre d’éléments qui sont activés et aide à éviter de manquer de ressources système si l’utilisateur ouvre un trop grand nombre de fenêtres.

## <a name="remarks"></a>Notes

Lorsque le nombre d’éléments sélectionnés ne correspond pas au modèle de sélection de verbe ou est supérieur aux limites par défaut indiquées dans le tableau suivant, le verbe ne s’affiche pas.



| Type d’implémentation de verbe | Document | Lecteur    |
|-----------------------------|----------|-----------|
| Hérité                      | 15 éléments | 100 éléments |
| COM                         | 15 éléments | Aucune limite  |



 

Voici des exemples d’entrées de Registre qui utilisent la valeur MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



