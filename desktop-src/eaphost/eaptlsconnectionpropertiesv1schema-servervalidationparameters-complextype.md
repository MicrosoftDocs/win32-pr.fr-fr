---
title: Type complexe ServerValidationParameters (TLS)
description: En savoir plus sur le type complexe ServerValidationParameters. Ce type contient des informations sur la façon d’effectuer la validation du serveur. | Type complexe ServerValidationParameters (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
keywords:
- ServerValidationParameters type complexe EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543556"
---
# <a name="servervalidationparameters-complex-type-tls"></a>Type complexe ServerValidationParameters (TLS)

Le type complexe **ServerValidationParameters** contient des informations sur la façon d’effectuer la validation du serveur.

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                                                                    | Type      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean   | Indique si la validation du serveur doit être demandée à l’utilisateur. <br/> Si [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur true, EAP-TLS effectue la validation du serveur sans entrée d’utilisateur ; Si la validation échoue, l’authentification EAP-TLS échoue. <br/> Si [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine.<br/> L’élément [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) est facultatif.<br/> |
| [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | string    | Représente une liste de serveurs approuvés par le client. Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières.<br/> L’élément [**serverNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary | Capture l’impression Thumb des autorités de certification racines approuvées par le client. <br/> L’impression Thumb est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.<br/> L’élément [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Types complexes de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





