---
title: Élément Task (DefinitionType)
description: Définit un événement spécifique à la tâche que votre fournisseur peut journaliser. | Élément Task (DefinitionType)
ms.assetid: 0e880720-1896-43cf-b702-cabca8ab1430
keywords:
- élément Task EventLog
topic_type:
- apiref
api_name:
- task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35fe629c17b8ede4064de3fb11d05c8e8c84f202
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527069"
---
# <a name="task-definitiontype-element"></a>Élément Task (DefinitionType)

\[À partir du compilateur de messages fourni avec la version Windows 7 du SDK Windows, cet élément n’est plus disponible.\]

Définit un événement spécifique à la tâche que votre fournisseur peut journaliser.

``` syntax
<xs:element name="task"
    type="TaskEventDefinitionType"
 />
```

L’élément **Task** est défini par le type complexe [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**événements (ProviderType)**](eventmanifestschema-events-providertype-element.md)
</dt> </dl>

 

 





