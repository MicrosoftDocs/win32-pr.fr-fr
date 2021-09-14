---
description: En savoir plus sur le paramètre PageBlackGenerationProcessingBlackInkLimit. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118017"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a>PageBlackGenerationProcessingBlackInkLimit

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le contenu de l’application étiqueté avec la couleur nommée spécifiée doit apparaître dans toutes les séparations de couleurs.

-   [Informations sur les éléments](#element-information)
-   [Structure de contenu](#structure-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|------------------------------------------------------------|
| Type d'élément <br/>   | ParameterDef<br/>                                    |
| Préfixe d’étendue <br/> | Page<br/>                                            |
| Notes <br/>          | Lié à l’élément PageBlackGenerationProcessing<br/> |



 

## <a name="structure-content"></a>Structure de contenu

La structure XML de cet élément est :

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>Propriétés de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Propriété                | xsi:type           | Valeur                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | string<br/>  | non défini<br/>       |
| MaxValue<br/>     | entier<br/> | 100<br/>             |
| MinValue<br/>     | entier<br/> | 0<br/>               |
| Multiple<br/>     | integer<br/> | 1<br/>               |
| Obligatoire<br/>    | string<br/>  | PSK : conditionnel<br/> |
| Unité<br/>     | string<br/>  | pour cent<br/>         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




