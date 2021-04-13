---
description: ICEM02 vérifie que toutes les dépendances et exclusions de module sont liées au module en cours.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201792"
---
# <a name="icem02"></a>ICEM02

ICEM02 vérifie que toutes les dépendances et exclusions de module sont liées au module en cours.

Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.

## <a name="result"></a>Résultats

ICEM02 publie des messages d’erreur si la base de données du module tente de spécifier des dépendances ou des exclusions qui ne sont pas liées au module en cours. ICEM02 publie un message d’erreur si la base de données du module tente de spécifier le module en cours comme dépendant ou comme étant exclu par lui-même.

## <a name="example"></a>Exemple

ICEM02 publie les messages d’erreur suivants pour un module contenant les entrées de base de données indiquées ci-dessous.

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[ModuleSignature, table](modulesignature-table.md)



| ModuleID         | Langage | Version |
|------------------|----------|---------|
| MyModule. *Guid1* | 1033     | 1.0     |



 

[Table ModuleDependency](moduledependency-table.md)



| ModuleID            | ModuleLanguage | RequiredID          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *GUID2* | 1033           | OtherModule. *GUID3* | 0                | 1.0             |
| MyModule. *Guid1*    | 1033           | MyModule. *Guid1*    | 1033             | 1.2             |



 

[Table ModuleExclusion](moduleexclusion-table.md) (partielle)



| ModuleID            | ModuleLanguage | ExcludedID          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *GUID2* | 1033           | OtherModule. *GUID3* | 0                |
| MyModule. *Guid1*    | 1033           | MyModule. *Guid1*    | 1033             |



 

Le module de fusion ICE publie la première erreur en raison de la de la première ligne dans la table ModuleDependency, qui ne spécifie pas de dépendance requise pour le module en cours spécifié dans la table ModuleSignature. Les dépendances d’un module ne peuvent être spécifiées que dans sa propre table ModuleDependency. Si OtherModule. *GUID3* est requis par le module en cours, remplacez les deux premières colonnes de la ligne par les données de la table ModuleSignature. Si OtherModule. *GUID3* n’est pas requis par ce module, supprimez cette ligne.

Le module de fusion ICE publie la deuxième erreur, car un module ne peut pas spécifier une dépendance sur lui-même.

Le module de fusion ICE publie la troisième erreur en raison de la première ligne dans la table ModuleExclusion, qui ne spécifie pas d’exclusion requise pour le module en cours spécifié dans la table ModuleSignature. Les exclusions d’un module ne peuvent être spécifiées que dans sa propre table ModuleExclusion. Si le module en cours exclut OtherModule. *GUID3*, remplacez les deux premières colonnes de la ligne par les données de la table ModuleSignature. Si le module actuel n’exclut pas OtherModule. *GUID3*, supprimez cette ligne.

Le module de fusion ICE publie la quatrième erreur, car un module ne peut pas spécifier qu’il s’exclut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



