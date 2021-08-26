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
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032009"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Requête (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





