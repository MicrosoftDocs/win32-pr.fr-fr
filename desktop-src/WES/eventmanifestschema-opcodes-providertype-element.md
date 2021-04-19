---
title: OpCodes (ProviderType), élément
description: Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche. | OpCodes (ProviderType), élément
ms.assetid: 28f67c43-053d-42e6-81eb-2353cc3898af
keywords:
- OpCodes, élément EventLog
topic_type:
- apiref
api_name:
- opcodes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b551f1158e58cb671a0fb872f73eabec1b29de33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531479"
---
# <a name="opcodes-providertype-element"></a>OpCodes (ProviderType), élément

Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche.

``` syntax
<xs:element name="opcodes"
    type="OpcodeListType"
 />
```

L’élément **OpCodes** est défini par le type complexe [**ProviderType**](eventmanifestschema-providertype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**fournisseur (EventsType)**](eventmanifestschema-provider-eventstype-element.md)
</dt> </dl>

 

 





