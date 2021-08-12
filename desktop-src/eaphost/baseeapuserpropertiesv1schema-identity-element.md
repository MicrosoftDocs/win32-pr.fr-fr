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
ms.openlocfilehash: ad88e84583be2b392ce8a4dfdaec7495f1c063fa13d4327004bfbecbc1f925ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275466"
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



| Rôle | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





