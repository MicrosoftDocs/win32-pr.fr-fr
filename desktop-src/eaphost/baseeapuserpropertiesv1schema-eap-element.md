---
title: Élément EAP (propriété utilisateur)
description: En savoir plus sur l’élément EAP. Cet élément capture le type de méthode sélectionné et la configuration spécifique à la méthode. | Élément EAP (propriété utilisateur)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- Élément EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 877f7b00953bff6cbac585fc549e9fa44d1ba98e89720b2d1a8317c2538ed64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275692"
---
# <a name="eap-element-user-property"></a>Élément EAP (propriété utilisateur)

L’élément **EAP** capture le type de méthode sélectionné et la configuration spécifique à la méthode.

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Notes

La méthode peut définir les éléments constitutifs à l’intérieur de l’élément **EAP** . La méthode effectue également une validation de schéma sur les éléments dans **EAP**.

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

 

 





