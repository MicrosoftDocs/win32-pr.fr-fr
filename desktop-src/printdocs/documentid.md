---
description: En savoir plus sur l’élément DocumentID, qui spécifie un ID unique pour le document. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 6e7899e3-9b64-48bd-8683-aba627458f2a
title: DocumentID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d309045db166901b9f521dd5a98cc47969190f54f8872818b33a8967a499b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447589"
---
# <a name="documentid"></a>DocumentID

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Spécifie un ID unique pour le document.

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|---------------------|
| Type d'élément <br/>   | Propriété<br/> |
| Préfixe d’étendue <br/> | Document<br/> |
| Notes <br/>          | Aucun<br/>     |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est la suivante :

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string">_DocumentIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                           | Type de données         | Unité | Valeurs prises en charge | Récapitulatif |
|--------------------------------|-------------------|------|------------------|---------|
| \_DocumentIDValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

``` syntax
<psf:Property name="psk:DocumentID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




