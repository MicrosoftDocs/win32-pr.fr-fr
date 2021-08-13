---
title: Élément EapHostConfig
description: Contient l’élément EapMethod et l’élément config ou ConfigBlob. Les éléments config et ConfigBlob ne peuvent pas être utilisés simultanément.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Élément EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c34ddd1607a59c0425f7ec789bedb4981a05983ead276a14308fbf6aaadf26de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274863"
---
# <a name="eaphostconfig-element"></a>Élément EapHostConfig

L’élément **EapHostConfig** contient l’élément [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) et l’élément [**config**](eaphostconfigschema-config-eaphostconfig-element.md) ou [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .

Les éléments [**config**](eaphostconfigschema-config-eaphostconfig-element.md) et [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) ne peuvent pas être utilisés simultanément.

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                    | Type                                                                                     | Description                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**Package**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**BaseEapMethodConfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Est utilisé lorsque la configuration de la méthode est au format texte XML au lieu d’un objet BLOB binaire.<br/>       |
| [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Est utilisé lorsque la configuration de la méthode est sous forme d’objet BLOB binaire au lieu d’une chaîne de texte.<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                       | Identifie la méthode référencée. <br/>                                                 |



## <a name="remarks"></a>Notes

L’élément **processContents** active les futures améliorations du schéma. L’élément **processContents** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





