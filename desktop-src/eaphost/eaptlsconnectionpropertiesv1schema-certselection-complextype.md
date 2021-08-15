---
title: Type complexe CertSelection
description: En savoir plus sur le type complexe CertSelection. Ce type détermine la façon dont l’utilisateur sélectionne un certificat.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection type complexe EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 375ea26fddf07f8d775617c0a2167ed02aa8160de8cc5dde49a92f37f57a335e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984129"
---
# <a name="certselection-complex-type"></a>Type complexe CertSelection

Le type complexe **CertSelection** détermine la façon dont l’utilisateur sélectionne un certificat.

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                     | Type    | Description                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | boolean | A la valeur TRUE par défaut. Si [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) a la valeur true, EAP-TLS effectue une recherche de certificat simple sans liste déroulante pour la sélection des certificats. Si **SimpleCertSelection** a la valeur false, EAP-TLS illustre à l’utilisateur le certificat approprié à sélectionner.<br/> |



## <a name="requirements"></a>Configuration requise



| Fonction | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Types complexes de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





