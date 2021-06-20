---
description: Les instances ScoredProperty peuvent également être imbriquées dans d’autres instances ScoredProperty ou en tant qu’éléments enfants d’une instance d’option.
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: Instances ScoredProperty imbriquées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a80d291fa59b2f36191f42b2f99ea9d22789a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408602"
---
# <a name="nested-scoredproperty-instances"></a>Instances ScoredProperty imbriquées

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Notez que vous n’êtes pas limité à l’ajout d’instances ScoredProperty en tant qu’éléments enfants d’une instance d’option. Les instances ScoredProperty peuvent également être imbriquées dans d’autres instances ScoredProperty. Cela est utile quand une propriété de l’appareil est complexe et est mieux représentée par plusieurs sous-propriétés. L’ajout de sous-propriétés à une propriété (ou publique) existante ou à un ScoredProperty est un bon moyen d’améliorer une option, tout en conservant la portabilité avec les instances d’option existantes. Par exemple, les instances d’option standard pour la fonctionnalité MediaType contiennent un ScoredProperty décrivant le poids du média comme clair, moyen, lourd ou ExtraHeavy. Si vous souhaitez obtenir des descriptions plus précises du poids, vous pouvez ajouter une sous-propriété (GramsPer100Sheets dans l’exemple suivant) qui contient le poids réel (en grammes) de feuilles de 100 de médias. L’option Enhanced peut se présenter comme dans l’exemple suivant.

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

Une comparaison des instances d’options d’origine et améliorées produit une correspondance presque parfaite, car l’option améliorée est un sur-ensemble de l’original, et les emplacements et valeurs de chacune des instances ScoredProperty d’origine sont conservés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



