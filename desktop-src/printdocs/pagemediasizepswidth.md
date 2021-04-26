---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4399b75f047c2705983c893075995800396120
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997546"
---
# <a name="pagemediasizepswidth"></a>PageMediaSizePSWidth

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Spécifie la largeur de la page perpendiculairement au sens de l’orientation du flux (référence [PostScript Printer Description file format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).

-   [Informations sur les éléments](#element-information)
-   [Structure de contenu](#structure-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Value |
|----------------------------|-------------------------------------------------------------|
| Type d'élément <br/>   | ParameterDef<br/>                                     |
| Préfixe d’étendue <br/> | Page<br/>                                             |
| Notes <br/>          | Lié à l’élément PageMediaSize, option CustomPS<br/> |



 

## <a name="structure-content"></a>Structure de contenu

La structure XML de cet élément est :

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriétés de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Propriété                | xsi:type           | Value                      |
|-------------------------|--------------------|----------------------------|
| DataType<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | entier<br/> | non défini<br/>       |
| MaxValue<br/>     | entier<br/> | non défini<br/>       |
| MinValue<br/>     | entier<br/> | non défini<br/>       |
| Obligatoire<br/>    | string<br/>  | PSK : conditionnel<br/> |
| Plusieurs<br/>     | integer<br/> | 1<br/>               |
| Unité<br/>     | string<br/>  | microns<br/>         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification de format de fichier de description d’imprimante PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




