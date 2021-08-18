---
title: Type simple GUIDType (schéma d’événement)
description: Définit un type d’identificateur global unique, au format de registre. | Type simple GUIDType (schéma d’événement)
ms.assetid: dbc305ef-6f07-4a70-9013-b89ccec889ea
keywords:
- Journal des types simples GUIDType
topic_type:
- apiref
api_name:
- GUIDType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fb7c0cd759b8b58b0db801819ed365f5b25fdb5abdcf886430e8bb2582cbde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750621"
---
# <a name="guidtype-simple-type-event-schema"></a>Type simple GUIDType (schéma d’événement)

Définit un type d’identificateur global unique, au format de registre.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **GUIDType** est une chaîne qui est limitée par le modèle suivant :

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    La valeur doit être un type d’identificateur global unique au format du Registre. Par exemple, {5b2fc63a-8AF4-44cb-960C-aefdced908d6}. Utilisez GUIDGen.exe ou UUIDGen.exe pour créer un GUID.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





