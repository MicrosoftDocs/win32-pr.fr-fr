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
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385147"
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



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Requête (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





