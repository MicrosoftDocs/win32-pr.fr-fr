---
title: Élément Suppress (QueryType)
description: Requête XPath qui identifie les événements à exclure du jeu de résultats de la requête.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Supprimer l’élément EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106330"
---
# <a name="suppress-querytype-element"></a>Élément Suppress (QueryType)

Requête XPath qui identifie les événements à exclure du jeu de résultats de la requête.

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

L’élément de **suppression** est défini par le type complexe [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Path | anyURI | Nom du canal ou chemin d’accès au fichier journal qui contient les événements.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Requête (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





