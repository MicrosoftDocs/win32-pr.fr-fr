---
title: Type complexe BaseEapParameters-propriétés de l’utilisateur
description: Définit l’élément qui a spécifié la méthode héritée sélectionnée et les informations d’identification spécifiques à la méthode.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
keywords:
- BaseEapParameters type complexe EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106527967"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Type complexe BaseEapParameters-propriétés de l’utilisateur

Le type complexe **BaseEapParameters** définit l’élément qui a spécifié la méthode héritée sélectionnée et les informations d’identification spécifiques à la méthode.

La méthode peut définir les éléments constitutifs à l’intérieur de **BaseEapParameters**; la méthode effectue également une validation de schéma sur les éléments dans **BaseEapParameters**.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                      | Type    | Description                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**Type**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | entier | Définit l’élément d’espace réservé pour le type de méthode sélectionné et les informations d’identification spécifiques à la méthode. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





