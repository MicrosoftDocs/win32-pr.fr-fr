---
description: La table FeatureComponents définit la relation entre les fonctionnalités et les composants. Pour chaque fonctionnalité, ce tableau répertorie tous les composants qui composent cette fonctionnalité.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Table FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7635a43784ee7e8fbb71c7161bb07d39ffe5238177ea2a7cdaabdeb18dc41e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430869"
---
# <a name="featurecomponents-table"></a>Table FeatureComponents

La table FeatureComponents définit la relation entre les fonctionnalités et les composants. Pour chaque fonctionnalité, ce tableau répertorie tous les composants qui composent cette fonctionnalité.

La table FeatureComponents contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Fonctionnalité\_   | [Identificateur](identifier.md) | O   | N        |
| -\_ | [Identificateur](identifier.md) | O   | N        |



 

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

## <a name="remarks"></a>Remarques

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

 

 



