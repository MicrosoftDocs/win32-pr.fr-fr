---
description: En savoir plus sur l’élément DocumentCoverBackSource, qui spécifie la source d’une feuille de couverture principale personnalisée.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be16ab26a4aa3dd7109fee7d630ed354b9b686d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409352"
---
# <a name="documentcoverbacksource"></a>DocumentCoverBackSource

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Spécifie la source d’une feuille de couverture principale personnalisée.

-   [Informations sur les éléments](#element-information)
-   [Structure de contenu](#structure-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|------------------------------------------------|
| Type d'élément <br/>   | ParameterDef<br/>                        |
| Préfixe d’étendue <br/> | Document<br/>                            |
| Notes <br/>          | Lié à l’élément DocumentCoverBack<br/> |



 

## <a name="structure-content"></a>Structure de contenu

La structure XML de cet élément est :

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a>Propriétés de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Propriété                | xsi:type           | Valeur                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | non défini<br/>       |
| MaxLength<br/>    | entier<br/> | non défini<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Obligatoire<br/>    | string<br/>  | PSK : conditionnel<br/> |
| Unité<br/>     | string<br/>  | caractères<br/>      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




