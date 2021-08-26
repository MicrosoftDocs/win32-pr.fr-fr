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
ms.openlocfilehash: 83b49427e65bb5190554a0c995bec119de1230f0baab869ea4c5ce48dc5616f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008969"
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

## <a name="remarks"></a>Remarques

Les valeurs valides sont « normal » et « inerte ».

Si le type est « inerte », le contenu contenu est une page de journal qui est l’arrière-plan en lecture seule/non modifiable pour le document. Cela se produit lorsqu’un document est créé à l’aide du pilote d’imprimante du rédacteur de note de journal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                     |



 

 




