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
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519732"
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

## <a name="remarks"></a>Notes

La méthode EAP effectue une validation de schéma sur le contenu de l’élément **BaseEapMethodConfig** .

## <a name="requirements"></a>Spécifications



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

 

 





