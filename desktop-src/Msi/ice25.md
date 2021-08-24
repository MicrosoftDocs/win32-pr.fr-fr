---
description: ICE25 vérifie qu’un fichier .msi satisfait à toutes ses dépendances et exclusions de module de fusion internes.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2715ce629ad22b872b8d38d0c6848236b9f1af9378a0a652b702e7b72cbd7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528949"
---
# <a name="ice25"></a>ICE25

ICE25 vérifie qu’un fichier .msi satisfait à toutes ses dépendances et exclusions de [module de fusion](merge-modules.md) internes. ICE valide les éléments suivants :

-   Toutes les dépendances de module de fusion indiquées dans la [table ModuleDependency](moduledependency-table.md) du fichier .msi sont satisfaites par au moins un module de fusion répertorié dans la [table ModuleSignature](modulesignature-table.md).
-   Aucun module de fusion exclu dans la [table ModuleExclusion](moduleexclusion-table.md) n’est pas compatible avec les modules de fusion répertoriés dans la [table ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Résultat

ICE25 publie un message d’erreur si .msi fichier a été précédemment fusionné avec un module de fusion incompatible ou s’il n’a pas été fusionné avec un module de fusion nécessaire.

## <a name="example"></a>Exemples

ICE25 publie les erreurs suivantes pour l’exemple indiqué.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[ModuleSignature, table](modulesignature-table.md)



| ModuleID | Langage | Version |
|----------|----------|---------|
| Module  | 0        | 1.0     |
| ModuleB  | 1033     | 1.0     |



 

[Table ModuleDependency](moduledependency-table.md)



| ModuleID | ModuleLanguage | RequiredID | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Module  | 0              | ModuleX    | 0                | 2.0             |



 

[Table ModuleExclusion](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | ExcludedID | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Module  | 0              | ModuleB    | 1033             |                    |                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



