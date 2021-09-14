---
description: ICE41 vérifie que les entrées dans les tables de classes et d’extensions font référence aux entrées de la table de composants qui implémentent l’objet de classe ou l’extension du composant.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021560"
---
# <a name="ice41"></a>ICE41

ICE41 vérifie que les entrées dans les tables de [classes](class-table.md) et d' [Extensions](extension-table.md) font référence aux entrées de la [table de composants](component-table.md) qui implémentent l’objet de classe ou l’extension du composant.

## <a name="result"></a>Résultats

ICE41 publie une erreur s’il existe une fonctionnalité qui ne contient pas le composant qui implémente l’extension ou l’objet de classe.

## <a name="example"></a>Exemple

ICE41 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE41                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| {00000000-0000-0000-0000-0000000000000}La classe référence la fonctionnalité feature2 et le composant Composant1, mais ce composant n’est pas associé à cette fonctionnalité dans la table FeatureComponents. | Il existe une fonctionnalité qui ne contient pas le composant qui implémente l’objet de classe. Cela signifie que le programme d’installation n’installe pas le composant avec la fonctionnalité et que la publicité peut ne pas fonctionner comme prévu. Pour corriger cette erreur, modifiez l’entrée dans la colonne Feature \_ de l’entrée de la [table de classes](class-table.md) afin de faire référence à une fonctionnalité qui installe le composant figurant dans la \_ colonne composant ou modifiez la fonctionnalité et le composant associés dans la [table FeatureComponents](featurecomponents-table.md).<br/>          |
| Extension. Yip fait référence à Feature1 et au composant COMPONENT2, mais ce composant n’est pas associé à cette fonctionnalité dans la table FeatureComponents.                                | Il existe une fonctionnalité qui ne contient pas le composant qui implémente l’extension. Cela signifie que le programme d’installation n’installe pas le composant avec la fonctionnalité et que la publicité peut ne pas fonctionner comme prévu. Pour corriger cette erreur, modifiez l’entrée dans la colonne Feature \_ de l’entrée de la [table d’extension](extension-table.md) pour faire référence à une fonctionnalité qui installe le composant figurant dans la \_ colonne composant ou modifiez la fonctionnalité et le composant associés dans la [table FeatureComponents](featurecomponents-table.md).<br/> |



 

[Table FeatureComponents](featurecomponents-table.md) (partielle)



| Fonctionnalité\_ |
|-----------|
| Feature1  |
| Feature2  |



 

[Table de classe](class-table.md) (partielle)



| CLSID                                  | Composant\_ | Fonctionnalité\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Composant1  | Feature2  |



 

[Table de classe](class-table.md) (partielle)



| Extension | Composant\_ | Fonctionnalité\_ |
|-----------|-------------|-----------|
| .yip      | Component2  | Feature1  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




