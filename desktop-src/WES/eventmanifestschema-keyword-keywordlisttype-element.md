---
title: Keyword (élément KeywordListType)
description: Définit un mot clé qui identifie une catégorie d’événements. | Keyword (élément KeywordListType)
ms.assetid: c921eb01-f1b0-455c-8ff9-06895f1e40f9
keywords:
- Keyword, élément EventLog
topic_type:
- apiref
api_name:
- keyword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4b1b0b60502339db55c3227add9bb5a263200aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523140"
---
# <a name="keyword-keywordlisttype-element"></a>Keyword (élément KeywordListType)

Définit un mot clé qui identifie une catégorie d’événements. Un mot clé est une balise que vous attachez à un événement pour regrouper des événements en fonction de leur utilisation.

``` syntax
<xs:element name="keyword"
    type="KeywordType"
 />
```

L’élément de **mot clé** est défini par le type complexe [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Éléments parents**
</dt> <dt>

[**Mots clés (ProviderType)**](eventmanifestschema-keywords-providertype-element.md)
</dt> <dt>

[**Mots clés (type de données)**](eventmanifestschema-keywords-metadatatype-element.md)
</dt> </dl>

 

 





