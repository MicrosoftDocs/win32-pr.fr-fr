---
title: Élément EapType (eaptlsuserpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma baseeapuserpropertiesv1. Pour eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- Élément EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106545719"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Élément EapType (eaptlsuserpropertiesv1schema)

L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) du schéma [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Type      | Description                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom d’utilisateur**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Capture le nom d’utilisateur à envoyer dans la réponse EAP-Identity. Si l’élément [**username**](eaptlsuserpropertiesv1schema-username-element.md) est absent, EAP-TLS utilise le nom figurant dans le certificat auquel il est fait appel dans l’élément [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .<br/> |
| [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Fait référence au hachage SHA-1 du certificat qui doit être utilisé pour l’authentification.<br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a>Notes

L’élément **processContents** active les futures améliorations du schéma. L’élément **processContents** est facultatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





