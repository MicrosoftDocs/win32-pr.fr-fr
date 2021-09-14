---
description: ICE19 vérifie que les composants publiés font référence à un fichier dans la colonne keyPath de la table Component et qu’un raccourci publié fait référence à un répertoire dans cette colonne.
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021603"
---
# <a name="ice19"></a>ICE19

ICE19 vérifie que les composants publiés font référence à un fichier dans la colonne keyPath de la [table Component](component-table.md) et qu’un raccourci publié fait référence à un répertoire dans cette colonne.

ICE19 vérifie que les composants ou les raccourcis publiés ont un ComponentId. Les composants de la [table PublishComponent](publishcomponent-table.md), qui ne sont pas publiés dans une autre table, sont uniquement vérifiés pour voir s’ils ont un ComponentID.

## <a name="result"></a>Résultats

ICE19 publie un message d’erreur si la colonne keyPath de la table Component ne fait pas référence à un fichier dans le cas d’un composant publié ou d’un répertoire dans le cas d’un raccourci publié. ICE19 publie un message d’erreur si des composants ou des raccourcis publiés n’ont pas d’ID de composant.

## <a name="example"></a>Exemple

ICE19 publie les messages d’erreur suivants pour l’exemple illustré :

-   L’extension FLP fait référence au composant COMP1 qui n’a pas d’ID de l’élément spécifié dans la [table des composants](component-table.md).
-   L’extension exe référence le composant Comp4 qui fait référence à un répertoire comme son chemin d’accès keyPath. KeyPath a la valeur null dans la table des composants.
-   Le raccourci Shortcut2 fait référence au composant COMP3 qui fait référence à une entrée de registre en tant que chemin d’accès de clé. La valeur de la colonne attributs dans la table Component est 4.

[Table des composants](component-table.md) (partielle)



| Composant | ComponentId                            | Attributs | KeyPath |
|-----------|----------------------------------------|------------|---------|
| COMP1     | Null                                   | 0          | Fichier1   |
| COMP2     | {00000002-0003-0000-0000-624474736554} | 0          | Fichier2   |
| COMP3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[Table d’extension](extension-table.md) (partielle)



| Extension | Composant\_ |
|-----------|-------------|
| FLP       | COMP1       |
| TST       | COMP2       |
| exe       | Comp4       |



 

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Composant\_ | Fonctionnalité\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | ProductFeature |
| Shortcut2 | COMP3       | ProductFeature |



 

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité        |
|----------------|
| ProductFeature |



 

> [!Note]  
> Si l’extension FLP et exe font toutes deux référence au même composant, le serveur EXE ou COM qui les ouvre doivent être identiques. Ce fichier EXE est normalement le chemin d’accès du composant. Pour OFFICE, les extensions doc et xls ne peuvent pas faire référence au même composant, car le même EXE n’ouvre pas les deux extensions. Vous avez besoin d' winword.exe pour ouvrir les extensions de document et vous avez besoin d' excel.exe pour ouvrir les extensions xls.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



