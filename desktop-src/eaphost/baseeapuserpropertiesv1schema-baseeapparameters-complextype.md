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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519700"
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
| [**Entrer**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | entier | Définit l’élément d’espace réservé pour le type de méthode sélectionné et les informations d’identification spécifiques à la méthode. <br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





