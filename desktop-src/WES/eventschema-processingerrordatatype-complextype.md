---
title: Type complexe ProcessingErrorDataType
description: Définit une erreur qui s’est produite lors du rendu des données d’événement pour l’événement.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- ProcessingErrorDataType type complexe EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ee34e566bafa72812303fcb1f41b664a45aa77772e6ee818b9cb79bc94cbb51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904523"
---
# <a name="processingerrordatatype-complex-type"></a>Type complexe ProcessingErrorDataType

Définit une erreur qui s’est produite lors du rendu des données d’événement pour l’événement. Cela peut se produire si les données d’événement ne correspondent pas à la définition du modèle de données d’événement dans le manifeste.

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                          | Type        | Description                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [**Nom de l'élément de données**](eventschema-dataitemname-processingerrordatatype-element.md) | string      | Nom de l’élément de données d’événement à l’origine de l’erreur.<br/>                    |
| [**ErrorCode**](eventschema-errorcode-processingerrordatatype-element.md)       | unsignedInt | Code d’erreur de l’erreur qui s’est produite lors du rendu des données d’événement.<br/> |
| [**EventPayload**](eventschema-eventpayload-processingerrordatatype-element.md) | hexBinary   | Objet blob binaire qui contient l’intégralité des données d’événement.<br/>                        |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





