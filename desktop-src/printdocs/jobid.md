---
description: En savoir plus sur l’élément JobID, qui spécifie un ID unique pour le travail. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 138a0ae5-160d-46f2-91ae-596d8892351a
title: JobID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f60bbf5091f0e2f6f2da95482c3bca7004fc6e7e70817814d1c47a191aa9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971288"
---
# <a name="jobid"></a>JobID

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Spécifie un ID unique pour le travail.

-   [Informations sur les éléments](#element-information)
-   [Contenu structurel](#structural-content)
-   [Contenu Extensible Markup Language (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informations sur les éléments



| Nom | Valeur |
|----------------------------|---------------------|
| Type d'élément <br/>   | Propriété<br/> |
| Préfixe d’étendue <br/> | Travail<br/>      |
| Notes <br/>          | Aucun<br/>     |



 

## <a name="structural-content"></a>Contenu structurel

La structure XML de cet élément est :

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string">_JobIDValue_</psf:Value>
</psf:Property>
```

## <a name="structure-variables"></a>Variables de structure

Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.



| Nom                      | Type de données         | Unité | Valeurs prises en charge | Résumé |
|---------------------------|-------------------|------|------------------|---------|
| \_JobIDValue\_<br/> | string<br/> |      |                  |         |



 

## <a name="extensible-markup-language-xml-content"></a>Contenu Extensible Markup Language (XML)

``` syntax
<psf:Property name="psk:JobID">
    <psf:Value xsi:type="xs:string"></psf:Value> <!-- undefined -->
</psf:Property>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




