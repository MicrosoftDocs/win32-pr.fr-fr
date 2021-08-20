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
ms.openlocfilehash: 7750bdb9a5f3c2d6c187b0f765eeb9d7ad88c015403719c16d0b683637b10027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086943"
---
# <a name="eap-element-connection-properties"></a>Élément EAP (propriétés de connexion)

L’élément **EAP** capture le type de méthode sélectionné et la configuration spécifique à la méthode.

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Remarques

La méthode peut définir les éléments constitutifs à l’intérieur de l’élément **EAP** . La méthode effectue également une validation de schéma sur les éléments dans **EAP**.

## <a name="requirements"></a>Configuration requise



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

 

 





