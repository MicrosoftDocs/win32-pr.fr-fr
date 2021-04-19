---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409b101d944152fa28c8972da4d8515e8cdfb05b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520255"
---
# <a name="pagesourcecolorprofileembedded"></a>PageSourceColorProfileEmbedded

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Spécifie le profil de couleurs source incorporé.

-   [Informations sur les éléments](#element-information)
-   [Structure de contenu](#structure-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom                       |                                                     |
|----------------------------|-----------------------------------------------------|
| Type d'élément <br/>   | ParameterDef<br/>                             |
| Préfixe d’étendue <br/> | Page<br/>                                     |
| Notes <br/>          | Lié à l’élément PageSourceColorProfile<br/> |



 

## <a name="structure-content"></a>Structure de contenu

La structure XML de cet élément est :

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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

 

 




