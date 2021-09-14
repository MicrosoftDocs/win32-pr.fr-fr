---
description: ICEM05 vérifie que le module de fusion est correctement associé aux composants dans le module. Si vous associez de manière incorrecte un composant à un module, le composant n’est pas correctement associé à la base de données cible.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021434"
---
# <a name="icem05"></a>ICEM05

ICEM05 vérifie que le module de fusion est correctement associé aux composants dans le module. Si vous associez de manière incorrecte un composant à un module, le composant n’est pas correctement associé à la base de données cible.

Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.

## <a name="result"></a>Résultats

ICEM05 publie une erreur si la base de données du module associe de manière incorrecte des composants et le module.

## <a name="example"></a>Exemple

ICEM05 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[ModuleSignature, table](modulesignature-table.md)



| ModuleID         | Langage | Version |
|------------------|----------|---------|
| MyModule. *Guid1* | 1033     | 1.0     |



 

[**Table ModuleComponents**](modulecomponents-table.md)



| Composant  | ModuleID            | Langage |
|------------|---------------------|----------|
| Composant1 | MyModule. *Guid1*    | 1033     |
| Component2 | OtherModule. *GUID2* | 1033     |



 

[Table des composants](component-table.md) (partielle)



| Composant  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

Le module de fusion ICE signale la première erreur, car la table ModuleComponents tente d’associer un composant à un autre module qui n’est pas le module en cours spécifié dans la table ModuleSignature. Pour résoudre ce problème, remplacez les colonnes ModuleID et Language de l’enregistrement ModuleComponents pour COMPONENT2 par celles du module actuel, MyModule. *Guid1*.

Le module de fusion ICE signale la deuxième erreur, car le premier enregistrement de la table ModuleComponents tente d’associer Composant1 au module. Ce composant n’existe pas dans la table des composants du module de fusion. Un module ne peut être associé qu’à un composant qui existe dans le module. Pour résoudre ce problème, supprimez l’enregistrement du composant inexistant.

Le module de fusion ICE signale la troisième erreur, car le module tente d’ajouter Component3 à la base de données cible. Ce composant n’a pas été associé au module dans la table ModuleComponents. Pour corriger cette erreur, ajoutez un enregistrement pour Component3 à la table ModuleComponents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



