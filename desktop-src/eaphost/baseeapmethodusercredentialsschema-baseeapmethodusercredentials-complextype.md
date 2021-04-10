---
title: Type complexe BaseEapMethodUserCredentials
description: En savoir plus sur le type complexe BaseEapMethodUserCredentials. Ce type est un élément d’espace réservé pour les données d’informations d’identification de méthode.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730180"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Type complexe BaseEapMethodUserCredentials

Le type complexe **BaseEapMethodUserCredentials** est un élément d’espace réservé pour les données d’informations d’identification de méthode.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Notes

La méthode EAP effectue une validation de schéma sur le contenu de **BaseEapMethodUserCredentials**.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





