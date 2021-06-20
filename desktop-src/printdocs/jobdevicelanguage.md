---
description: En savoir plus sur l’élément JobDeviceLanguage, qui décrit les langues de l’appareil prises en charge pour l’envoi de données du pilote vers l’appareil physique.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7bf56018a2b395ec5aa182336a89d8872057e7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408993"
---
# <a name="jobdevicelanguage"></a>JobDeviceLanguage

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Décrit les langues de l’appareil prises en charge pour l’envoi de données du pilote vers l’appareil physique. Cela est souvent appelé « langage de description de page ». Ce mot clé définit le langage de description de page pris en charge par le pilote et l’appareil physique.

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|--------------------|
| Type d'élément <br/>   | Fonctionnalité<br/> |
| Préfixe d’étendue <br/> | Travail<br/>     |
| Notes <br/>          | Aucun<br/>    |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                                 | Type de données         | Unité                  | Valeurs prises en charge                                                                                                                                                                      | Résumé                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>            | string<br/> | caractères<br/> | Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.<br/> | Nom de l'option.<br/>                                           |
| \_IdentityOptionValue\_<br/>   | string<br/> | n/a<br/>        | True, False.<br/>                                                                                                                                                               | Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.<br/> |
| \_LanguageLevelValue\_<br/>    | string<br/> | n/a<br/>        | Aucun.<br/>                                                                                                                                                                      | Spécifie le niveau de langage (par exemple, PS de niveau 2).<br/>           |
| \_LanguageEncodingValue\_<br/> | string<br/> | n/a<br/>        | Aucun.<br/>                                                                                                                                                                      | Spécifie l’encodage de la langue (par exemple, ISOLatin1).<br/>         |
| \_LanguageVersionValue\_<br/>  | string<br/> | n/a<br/>        | Aucun.<br/>                                                                                                                                                                      | Spécifie la version du langage.<br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms. Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




