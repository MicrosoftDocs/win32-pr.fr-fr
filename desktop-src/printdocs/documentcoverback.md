---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 29d0bf2d-4897-43ed-ba3d-0b38b2f30375
title: DocumentCoverBack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5822921fe3dc1852100569b29a1ded8b37bc9aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994536"
---
# <a name="documentcoverback"></a>DocumentCoverBack

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Décrit la feuille de couverture Back (final). Chaque document aura une feuille distincte. La feuille de couverture doit être imprimée sur le PageMediaSize et le PageMediaType utilisés pour la dernière page du document. La feuille de couverture doit être intégrée dans les options de traitement (telles que DocumentDuplex, DocumentNUp), comme indiqué par l’option spécifiée.

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Value |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Type d'élément <br/>   | Fonctionnalité<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Préfixe d’étendue <br/> | Document<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Notes <br/>          | Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant. Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie. Ces paramètres sont spécifiques à XPS. <br/> Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL. Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.<br/> |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!--Specifies the XPS specific part name for the back cover sheet-->
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                               | Type de données         | Unité                  | Valeurs prises en charge                                                                                                                                                                      | Résumé                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caractères<br/> | Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.<br/> | Nom de l'option.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/a<br/>        | True, False.<br/>                                                                                                                                                               | Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms. Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :

``` syntax
<psf:Feature name="psk:DocumentCoverBack">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no cover will be output -->
  <psf:Option name="psk:NoCover" />
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the back side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBack">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" may be printed on either sides 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintBoth">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the cover indicated by "CoverBackSource" should be printed on the front side 
       of the cover sheet.  If a DocumentCoverBackSource ParameterInit element is not specified, 
       this Option should be ignored. -->
  <psf:Option name="psk:PrintFront">
    <psf:ScoredProperty name="psk:CoverBackSource">
      <psf:ParameterRef name="psk:DocumentCoverBackSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a blank cover sheet should be printed. -->
  <psf:Option name="psk:BlankCover" />
</psf:Feature>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




