---
title: Select (QueryType) (élément)
description: Requête XPath qui identifie les événements à inclure dans le jeu de résultats de la requête.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Sélectionner l’élément EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587402"
---
# <a name="select-querytype-element"></a>Select (QueryType) (élément)

Requête XPath qui identifie les événements à inclure dans le jeu de résultats de la requête.

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

L’élément **Select** est défini par le type complexe [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Path | anyURI | Nom du canal ou chemin d’accès au fichier journal qui contient les événements.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|-------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Requête (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





