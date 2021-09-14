---
description: La table FeatureComponents définit la relation entre les fonctionnalités et les composants. Pour chaque fonctionnalité, ce tableau répertorie tous les composants qui composent cette fonctionnalité.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Table FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091241"
---
# <a name="featurecomponents-table"></a>Table FeatureComponents

La table FeatureComponents définit la relation entre les fonctionnalités et les composants. Pour chaque fonctionnalité, ce tableau répertorie tous les composants qui composent cette fonctionnalité.

La table FeatureComponents contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Fonctionnalité\_   | [Identificateur](identifier.md) | O   | N        |
| Composant\_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_
</dt> <dd>

Clé externe dans la première colonne de la [table](feature-table.md)de fonctionnalités.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_
</dt> <dd>

Clé externe dans la première colonne de la [table de composants](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Il existe une limite maximale de 1600 composants par fonctionnalité.

Les composants peuvent être partagés par plusieurs fonctionnalités, autrement dit, un même composant peut être référencé par plusieurs fonctionnalités.

Cette table est référencée lorsque l' [action PublishFeatures](publishfeatures-action.md) ou l' [action UnpublishFeatures](unpublishfeatures-action.md) est exécutée.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



