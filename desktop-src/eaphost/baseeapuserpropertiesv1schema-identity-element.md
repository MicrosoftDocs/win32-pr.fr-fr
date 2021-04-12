---
title: Élément Identity
description: En savoir plus sur l’élément d’identité EAPHost. Cet élément capture l’identité utilisée pour l’authentification.
ms.assetid: 464979f0-6a2b-43e7-a207-2fbd1e2e5f51
keywords:
- Identity, élément EAPHost
topic_type:
- apiref
api_name:
- Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 485d576155d5ac63df2776016f3aafabf8c18c25
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463726"
---
# <a name="identity-element"></a>Élément Identity

L’élément **Identity** capture l’identité utilisée pour l’authentification.

``` syntax
<xs:element name="Identity"
    type="string"
 />
```

## <a name="remarks"></a>Notes

L’élément **Identity** est abstrait ; chaque méthode doit définir et utiliser un élément dérivé dans les documents d’instance.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





