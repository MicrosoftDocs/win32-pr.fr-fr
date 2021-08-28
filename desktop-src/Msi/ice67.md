---
description: ICE67 vérifie que la cible d’un raccourci non publié appartient au même composant que le raccourci lui-même, ou que les attributs du composant cible garantissent qu’il ne modifie pas les emplacements d’installation.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b25f3bba6bd6efaf20b55982524840348f39e8717dc53b7699a6f5f2886df01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787389"
---
# <a name="ice67"></a>ICE67

ICE67 vérifie que la cible d’un raccourci non publié appartient au même composant que le raccourci lui-même, ou que les attributs du composant cible garantissent qu’il ne modifie pas les emplacements d’installation.

Si vous ne corrigez pas un avertissement ou une erreur signalée par ICE67, le raccourci risque d’être non valide si le composant cible change d’État et que le composant source ne le fait pas. Par exemple, lorsque le composant du fichier cible est configuré pour s’exécuter à partir de la source, une réinstallation qui modifie le composant en local entraîne le non réinstallation du composant contenant le raccourci. Par conséquent, le raccourci pointe vers un emplacement non valide.

Notez que dans certains cas, l’utilisation d’un autre composant pour le raccourci est inévitable. Par exemple, si le raccourci est créé dans le profil utilisateur et que le fichier est installé dans un répertoire qui n’est pas du profil, vous risquez de ne pas pouvoir utiliser le même composant pour les deux éléments de données. (Cela entraîne des défaillances dans les scénarios multi-utilisateur, tels que ceux décrits dans [ICE57](ice57.md)). Dans ce cas, vous serez peut-être en mesure d’utiliser des raccourcis publiés pour obtenir le comportement souhaité, ou vous pouvez simplement vous assurer que le composant cible ne peut pas passer d’une exécution à une source à une source locale.

## <a name="result"></a>Résultat

ICE67 retourne une erreur ou un avertissement si la cible d’un raccourci non publié n’appartient pas au même composant que le raccourci lui-même, ou si les attributs du composant cible ne garantissent pas que les emplacements d’installation ne changeront pas.

## <a name="example"></a>Exemples

ICE67 signale les erreurs et avertissements suivants pour l’exemple indiqué.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 est installé par COMPONENT2, mais son fichier cible, fichier1, est installé par Composant1. Le composant cible est marqué comme étant facultatif (ce qui signifie qu’il peut être local ou d’exécution à partir de la source). Une situation susceptible de provoquer un problème est si Composant1 passe de l’exécution à partir de la source à la valeur locale. Shortcut1 ne peut alors pas pointer vers un emplacement non valide.

Pour résoudre cet avertissement, installez le raccourci dans le cadre de Composant1 ou marquez Composant1 comme LocalOnly ou SourceOnly.

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Composant\_ |
|-------|-------------|
| Fichier1 | Composant1  |



 

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Composant\_ | Cible      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#File1\] |



 

[Table des composants](component-table.md) (partielle)



| Composant  | Attributs |
|------------|------------|
| Composant1 | 2          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



