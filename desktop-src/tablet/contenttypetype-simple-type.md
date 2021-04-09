---
description: Définit le type qui définit des valeurs valides pour l’attribut de type du lecteur du journal des éléments de contenu \[ \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Type simple ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034666"
---
# <a name="contenttypetype-simple-type"></a>Type simple ContentTypeType

Définit le type qui définit des valeurs valides pour l’attribut de *type* du [ \[ lecteur \] du journal des éléments de contenu](content-element--journal-reader.md).

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **ContentTypeType** est une chaîne qui est limitée par le modèle suivant :

-   `Normal|Inert`

## <a name="remarks"></a>Notes

Les valeurs valides sont « normal » et « inerte ».

Si le type est « inerte », le contenu contenu est une page de journal qui est l’arrière-plan en lecture seule/non modifiable pour le document. Cela se produit lorsqu’un document est créé à l’aide du pilote d’imprimante du rédacteur de note de journal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 




