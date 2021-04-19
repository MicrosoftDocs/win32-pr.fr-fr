---
description: ICE62 effectue des vérifications approfondies sur la table IsolatedComponent pour les données susceptibles de provoquer un comportement inattendu.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544975"
---
# <a name="ice62"></a>ICE62

ICE62 effectue des vérifications approfondies sur la [table IsolatedComponent](isolatedcomponent-table.md) pour les données susceptibles de provoquer un comportement inattendu.

Si vous ne corrigez pas une erreur signalée par ICE62, vous risquez de provoquer une défaillance du système de composants isolés de plusieurs façons. Par exemple, si le bit SharedDllRefCount n’est pas défini pour un composant partagé, l’inscription du composant peut être supprimée lorsqu’une autre application utilise ce ComponentId et est désinstallée.

## <a name="result"></a>Résultats

ICE62 publie un avertissement ou une erreur lorsqu’il trouve des données dans la table IsolatedComponent qui peuvent produire un comportement inattendu.

## <a name="example"></a>Exemple

ICE62 signale les erreurs et avertissements suivants pour les exemples indiqués.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

COMPONENT2 est listé comme composant d’application pour l’isolation de Composant1. Toutefois, COMPONENT2 a un chemin d’accès de clé de Registre et ne fournit pas de chemin d’accès d’exécutable valide à utiliser pour isoler le composant.

Pour corriger cette erreur, utilisez un autre composant que l’application pour le composant isolé Composant1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Composant1 est listé comme un composant partagé isolé, mais le bit SharedDllRefCount n’est pas défini. Cela peut entraîner une inexactitude de la durée de vie du composant. Si une autre application utilise ce composant (isolé ou non) et qu’elle est désinstallée, l’inscription du composant est supprimée, mais la copie isolée de cette application est conservée. Cela entraîne des problèmes de réparation et de désinstallation.

Pour corriger cette erreur, définissez le bit SharedDllRefCount pour le composant.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Composant1 et COMPONENT2 sont installés par différentes fonctionnalités. Composant1 est installé par Feature1 et COMPONENT2 est installé par feature2. Feature1 n’est pas un parent de feature2. par conséquent, il est possible d’installer l’application, mais pas le composant isolé, ce qui rompt l’isolation.

Pour corriger cette erreur, ajoutez une entrée à la table FeatureComponents qui lie Composant1 à la même fonctionnalité que (ou une fonctionnalité parente de) la fonctionnalité qui installe COMPONENT2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Composant1 a une condition dans la table des composants. Si cette condition passe de TRUE à FALSe pendant la durée de vie d’une installation sur un ordinateur, le composant isolé peut être orphelin sans les informations d’inscription.

Pour résoudre cet avertissement, supprimez la condition ou créez la condition de sorte qu’elle ne puisse jamais passer de TRUE à FALSe.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Composant1 est isolé pour COMPONENT2 et Component3, et les deux composants sont également installés dans le même répertoire. Les applications partagent un composant isolé, mais si une application est supprimée, le composant partagé est également supprimé, ce qui entraîne la perte du composant isolé par les autres applications.

Pour résoudre cet avertissement, installez les applications dans différents répertoires ou vérifiez si certaines des applications nécessitent véritablement un composant isolé.

[Table IsolatedComponent](isolatedcomponent-table.md)



| Composant \_ partagé | Application de composant \_ |
|-------------------|------------------------|
| Composant1        | Component2             |
| Composant1        | Component3             |



 

[Table des composants](component-table.md)



| Composant  | ComponentId | Répertoire\_ | Attributs | Condition   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Composant1 |             | Dir1        | 0          | MYCONDITION | Fichier1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | Fichier3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Fonctionnalité\_ | -\_ |
|-----------|-------------|
| Feature1  | Composant1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité  | Parent de la fonctionnalité \_ |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



