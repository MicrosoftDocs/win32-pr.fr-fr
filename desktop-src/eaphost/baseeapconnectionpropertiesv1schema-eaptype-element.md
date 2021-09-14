---
title: Élément EapType (propriété de connexion de schéma v1)
description: En savoir plus sur l’élément EapType. Cet élément capture la configuration spécifique à la méthode à l’intérieur de l’élément EAP. | Élément EapType (propriété de connexion de schéma v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191967"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Élément EapType (propriété de connexion de schéma v1)

L’élément **EapType** capture la configuration spécifique à la méthode à l’intérieur de l’élément EAP.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Notes

L’élément **EapType** est abstrait ; chaque méthode doit définir et utiliser un élément dérivé dans les documents d’instance.

## <a name="requirements"></a>Spécifications



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





