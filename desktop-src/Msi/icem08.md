---
description: ICEM08 garantit qu’un module n’exclut pas un autre module dont il dépend.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c953c40d29458613b0fc2027dd691adb672eb15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021426"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantit qu’un module n’exclut pas un autre module dont il dépend.

## <a name="result"></a>Résultats

ICEM08 publie une erreur lorsqu’un module exclut un autre module dont il dépend.

## <a name="example"></a>Exemple

ICEM08 publie le message d’erreur suivant pour un module contenant les entrées de base de données indiquées dans l’exemple.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Table ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| Modulea. &lt; UNIQUES&gt; | 1033           | ModuleB. &lt; UNIQUES&gt; | 1033             | 1.0             |



 

[Table ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| Modulea. &lt; UNIQUES&gt; | 1033           | ModuleB. &lt; UNIQUES&gt; | 1033             |                    | 1.0                |



 

Pour corriger l’erreur, supprimez la dépendance ou l’exclusion. Si ModuleB est une dépendance (RequiredID) de modulea, vous ne pouvez pas l’exclure (comme indiqué dans la colonne ExludedID de la table ModuleExclusion). Si vous devez exclure ModuleB, vous devez supprimer la dépendance entre les modules.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



