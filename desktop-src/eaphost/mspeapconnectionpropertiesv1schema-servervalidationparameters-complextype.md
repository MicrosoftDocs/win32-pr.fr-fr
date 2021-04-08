---
title: Type complexe ServerValidationParameters (PEAP)
description: En savoir plus sur le type complexe ServerValidationParameters. Ce type contient des informations sur la façon d’effectuer la validation du serveur. | Type complexe ServerValidationParameters (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
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
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953540"
---
# <a name="servervalidationparameters-complex-type-peap"></a>Type complexe ServerValidationParameters (PEAP)

Le type complexe **ServerValidationParameters** contient des informations sur la façon d’effectuer la validation du serveur.

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                                                                    | Type        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean     | Indique si la validation du serveur doit être demandée à l’utilisateur. <br/> Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur true, PEAP effectue la validation du serveur sans entrée d’utilisateur ; en cas d’échec de la validation, l’authentification PEAP échoue.<br/> Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) a la valeur false, l’utilisateur est invité à fournir un certificat ou un nom de serveur validé, ou une autorité de certification racine (ca).<br/> L’élément [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) est facultatif.<br/> |
| [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | complexType | Représente une liste de serveurs approuvés par le client. Chaque nom de serveur est délimité par des points-virgules et peut être représenté par des expressions régulières. <br/> L’élément [**serverNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary   | Capture l’impression Thumb des autorités de certification racines approuvées par le client. <br/> L’impression Thumb est une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.<br/> L’élément [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) est facultatif.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a>Attributs



| Nom                    | Type    | Description                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PerformServerValidation | boolean | Windows 7 ou version ultérieure : indique si la validation du serveur est effectuée. L’élément [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) est facultatif.<br/> |



## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Types complexes de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[**AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





