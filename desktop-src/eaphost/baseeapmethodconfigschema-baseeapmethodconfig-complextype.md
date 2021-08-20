---
title: Type complexe BaseEapMethodConfig
description: En savoir plus sur le type complexe BaseEapMethodConfig. Ce type est un élément d’espace réservé pour la configuration de la méthode.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- BaseEapMethodConfig type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8decb1746391c1337440eb475a8a8face3f8b7466b73015db48e3991841a3c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086774"
---
# <a name="baseeapmethodconfig-complex-type"></a>Type complexe BaseEapMethodConfig

Le type complexe **BaseEapMethodConfig** est un élément d’espace réservé pour la configuration de la méthode.

``` syntax
<xs:complexType name="BaseEapMethodConfig">
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

## <a name="remarks"></a>Remarques

La méthode EAP effectue une validation de schéma sur le contenu de l’élément **BaseEapMethodConfig** .

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapmethodconfig](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





