---
description: ICE34 valide que chaque case d’option sur chaque contrôle RadioButtonGroup a une propriété dans la colonne propriété de la table RadioButton qui spécifie son groupe de cases d’option.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536484"
---
# <a name="ice34"></a>ICE34

ICE34 valide que chaque case d’option sur chaque [contrôle RadioButtonGroup](radiobuttongroup-control.md) a une propriété dans la colonne propriété de la [table RadioButton](radiobutton-table.md) qui spécifie son groupe de cases d’option. ICE34 valide que cette propriété existe et qu’elle est définie sur une valeur par défaut dans la [table de propriétés](property-table.md) qui est égale à l’une des valeurs de case d’option du groupe dans la colonne valeur de la table RadioButton.

Un groupe de cases d’option doit avoir une valeur par défaut pour que les utilisateurs puissent sélectionner un choix à l’aide de la touche TAB. Cela est nécessaire pour une accessibilité appropriée de l’utilisateur.

ICE34 signale les tables manquantes.

## <a name="result"></a>Résultats

ICE34 publiez un message d’erreur s’il existe une case d’option qui spécifie une propriété non valide.

## <a name="example"></a>Exemple

ICE34 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE34                                                                                                                                                                | Description                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La boîte de dialogue de contrôlea. Control2 doit avoir une propriété, car elle est de type RadioButtonGroup.                                                                                      | Il existe un [contrôle RadioButtonGroup](radiobuttongroup-control.md), sans le bit de [contrôle indirect](indirect-control-attribute.md) défini dans la colonne attributs de la [table de contrôle](control-table.md), pour laquelle aucune propriété n’est indiquée dans la colonne propriété. |
| Peut-être n’est pas une valeur par défaut valide pour RadioButtonGroup à l’aide de la propriété Property3. La valeur doit être indiquée en tant qu’option dans la table RadioButtonGroup.                 | Il existe une valeur par défaut pour une propriété spécifiée dans la colonne valeur de la [table de propriétés](property-table.md) qui ne fait pas partie des valeurs du groupe de cases d’option spécifié dans la colonne valeur de la [table RadioButton](radiobutton-table.md).                  |
| La propriété PropertyB doit être définie, car il s’agit d’une propriété indirecte d’une boîte de dialogue de contrôle RadioButtonGroupa. Control4                                                       | La propriété référencée par ce groupe RadioButton est une propriété indirecte et la valeur de la propriété indirect n’est pas l’un des choix du groupe RadioButton.                                                                                                       |
| Peut-être n’est pas une valeur par défaut valide pour la propriété PropertyA. La propriété est une propriété RadioButtonGroup indirecte de Control DIALOGA. Control5 (via la propriété Property5). | La valeur de la propriété indirecte référencée via le contrôle n’est pas l’une des valeurs par défaut pour ce RadioButtonGroup.                                                                                                                                                    |



 

[Table de contrôle](control-table.md) (partielle)



| Boîte de dialogue  | Contrôler  | Type             | Attributs | Propriété  |
|---------|----------|------------------|------------|-----------|
| Boîte de dialogue | Control1 | RadioButtonGroup | 0          | Property1 |
| Boîte de dialogue | Control2 | RadioButtonGroup | 0          |           |
| Boîte de dialogue | Control3 | RadioButtonGroup | 0          | Property3 |
| Boîte de dialogue | Control4 | RadioButtonGroup | 8          | Property4 |
| Boîte de dialogue | Control5 | RadioButtonGroup | 8          | Property5 |



 

[Table de propriétés](property-table.md) (partielle)



| Propriété  | Valeur     |
|-----------|-----------|
| Property1 | Oui       |
| Property3 | Peut-être     |
| Property4 | PropertyB |
| Property5 | Propriété |
| Propriété | Peut-être     |



 

[Table RadioButton](radiobutton-table.md) (partielle)



| Propriété  | Commande | Valeur |
|-----------|-------|-------|
| Property1 | 1     | Oui   |
| Property1 | 2     | maintenant   |
| Property2 | 1     | Oui   |
| Property2 | 2     | Non    |
| Property3 | 1     | Oui   |
| Property3 | 2     | Non    |
| Property4 | 1     | Oui   |
| Property4 | 2     | Non    |
| Propriété | 1     | Oui   |
| Propriété | 2     | Non    |
| PropertyB | 1     | Oui   |
| PropertyB | 2     | Non    |



 

Pour corriger les erreurs signalées par cette glace, vérifiez les points suivants :

-   Que chaque entrée de contrôle RadioButton sans l’ensemble d’attributs indirect a une propriété listée dans la colonne de propriété :
-   Que chaque propriété de ce type possède au moins une entrée correspondante dans la table de RadioButton.
-   Que chaque propriété de ce type est définie dans la table de propriétés, avec une valeur qui est l’un des choix de la table de RadioButton.
-   Chaque propriété référencée dans la colonne de propriété d’un contrôle RadioButton avec l’ensemble d’attributs indirect est définie dans la table de propriétés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



