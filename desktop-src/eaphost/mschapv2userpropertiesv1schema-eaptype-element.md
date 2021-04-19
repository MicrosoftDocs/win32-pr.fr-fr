---
title: Élément EapType (mschapv2userpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma baseeapuserpropertiesv1. Pour mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106530066"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a>Élément EapType (mschapv2userpropertiesv1schema)

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
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



| Élément                                                                           | Type   | Description                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom d’utilisateur**](mschapv2userpropertiesv1schema-username-element.md)               |        | Identifie l’utilisateur authentifié. Si cet élément n’est pas présent, le nom d’utilisateur est obtenu à partir de Winlogon. L’élément [**username**](mschapv2userpropertiesv1schema-username-element.md) est facultatif.<br/>                                        |
| [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | string | Identifie le domaine de l’utilisateur ou de l’ordinateur en cours d’authentification. Si cet élément n’est pas présent, c’est le domaine de Winlogon qui est utilisé. L’élément [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) est facultatif.<br/>        |
| [**De**](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | string | Identifie le mot de passe de l’utilisateur ou de l’ordinateur en cours d’authentification. Si cet élément n’est pas présent, le hachage de mot de passe est obtenu à partir de Winlogon. L’élément [**de mot de passe**](mschapv2userpropertiesv1schema-password-eaptype-element.md) est facultatif.<br/> |



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

[Schéma mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





