---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2c60fd005f42bd3f9861e86156a7da9164a81e
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106545221"
---
# <a name="jobdigitalsignatureprocessing"></a>JobDigitalSignatureProcessing

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Décrit la configuration du traitement de signature numérique pour l’ensemble du travail. S’applique uniquement au contenu qui contient des signatures numériques.

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom                       |                    |
|----------------------------|--------------------|
| Type d'élément <br/>   | Fonctionnalité<br/> |
| Préfixe d’étendue <br/> | Travail<br/>     |
| Notes <br/>          | Aucun<br/>    |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                               | Type de données         | Unité                   | Valeurs prises en charge                                                                                                                                                                      | Résumé                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | caractères <br/> | Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.<br/> | Nom de l’option<br/>                                            |
| \_IdentityOptionValue\_<br/> | string<br/> | n/a<br/>         | True, False<br/>                                                                                                                                                                | Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms. Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




