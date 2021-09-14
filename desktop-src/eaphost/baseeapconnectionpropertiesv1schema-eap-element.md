---
title: Élément EAP (propriétés de connexion)
description: En savoir plus sur l’élément EAP. Cet élément capture le type de méthode sélectionné et la configuration spécifique à la méthode. | Élément EAP (propriétés de connexion)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
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
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191971"
---
# <a name="eap-element-connection-properties"></a>Élément EAP (propriétés de connexion)

L’élément **EAP** capture le type de méthode sélectionné et la configuration spécifique à la méthode.

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Notes

La méthode peut définir les éléments constitutifs à l’intérieur de l’élément **EAP** . La méthode effectue également une validation de schéma sur les éléments dans **EAP**.

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

 

 





