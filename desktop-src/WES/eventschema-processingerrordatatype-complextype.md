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
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105178"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





