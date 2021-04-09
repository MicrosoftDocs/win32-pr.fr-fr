---
description: La UpgradeCode est principalement utilisée pour prendre en charge les mises à niveau majeures, bien que les correctifs de mise à niveau petit et mineur peuvent utiliser UpgradeCode pour la validation du produit.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Utilisation d’un UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf32d40364653527b9f906e6dd42de64bb9f697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864381"
---
# <a name="using-an-upgradecode"></a>Utilisation d’un UpgradeCode

La [**UpgradeCode**](upgradecode.md) est principalement utilisée pour prendre en charge les mises à niveau majeures, bien que les correctifs de mise à niveau petit et mineur peuvent utiliser **UpgradeCode** pour la validation du produit. Lors des mises à niveau majeures, les actions [FindRelatedProducts](findrelatedproducts-action.md), [MigrateFeatureStates](migratefeaturestates-action.md)et [RemoveExistingProducts](removeexistingproducts-action.md) détectent, migrent et suppriment les versions précédentes du produit. L’action FindRelatedProducts recherche des produits à l’aide de critères basés sur **UpgradeCode**, [**ProductLanguage**](productlanguage.md)et [**ProductVersion**](productversion.md). Ces critères sont spécifiés dans la table de [mise à niveau](upgrade-table.md) .

Étant donné les critères utilisés par l’action [FindRelatedProducts](findrelatedproducts-action.md) , la [**UpgradeCode**](upgradecode.md) peut être la même pour différents langages et versions d’un même produit. Cela est dû au fait que la table de [mise à niveau](upgrade-table.md) permet de différencier les produits selon les versions et les lignes de langue.

Dans les différentes versions du même produit, vous n’aurez peut-être jamais besoin de modifier la [**UpgradeCode**](upgradecode.md). Chaque produit autonome doit avoir sa propre **UpgradeCode**. Une suite de produits doit également avoir sa propre **UpgradeCode**. Cela permettra à la suite de mettre à niveau des versions antérieures de la suite ou des produits autonomes en utilisant plusieurs lignes dans la [table de mise à niveau](upgrade-table.md).

Les deux scénarios suivants illustrent l’utilisation de [**UpgradeCode**](upgradecode.md).

-   Le produit A et le produit B ont été livrés avec les mêmes [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md)et [**UpgradeCode**](upgradecode.md). Le produit A et le produit B ont des [**ProductCodes**](productcode.md)différents. Étant donné que les produits se voient attribuer le même **UpgradeCode**, la table de [mise à niveau](upgrade-table.md) ne peut pas être créée pour différencier l’ancienne version du produit A de l’ancienne version du produit B. Dans ce cas, vous ne pourrez pas effectuer une installation de mise à niveau du produit A qui ignore le produit B. Dans la mesure où il s’agissait de différents produits, chacun d’eux doit avoir reçu une autre **UpgradeCode**.
-   Les versions anglaise et française du produit A ont été fournies avec les mêmes [**ProductVersion**](productversion.md) et [**UpgradeCode**](upgradecode.md). Les versions anglaise et française du produit A ont des [**ProductLanguages**](productlanguage.md) et des [**ProductCodes**](productcode.md)différents. Bien que les versions en anglais et en français partagent la même **UpgradeCode**, il est possible de créer la table de [mise à niveau](upgrade-table.md) de façon à ce que seule l’ancienne version en langue anglaise soit détectée et mise à niveau et que la version française antérieure soit ignorée. Les différentes versions linguistiques d’un produit peuvent utiliser la même **UpgradeCode**.

 

 



