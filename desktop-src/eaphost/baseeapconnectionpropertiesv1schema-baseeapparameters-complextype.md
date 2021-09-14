---
title: Type complexe BaseEapParameters-propriétés de connexion
description: Définit l’élément d’espace réservé pour le type de méthode et la configuration spécifique à la méthode.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
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
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191976"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Type complexe BaseEapParameters-propriétés de connexion

Le type complexe **BaseEapParameters** définit l’élément d’espace réservé pour le type de méthode et la configuration spécifique à la méthode.

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



| Élément                                                                            | Type    | Description                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**Entrer**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | entier | Une instance de schéma est autorisée ici.<br/> |



## <a name="remarks"></a>Notes

Dans **BaseEapParameters** , la méthode peut définir les éléments constitutifs. La méthode effectue également une validation de schéma sur les éléments dans **BaseEapParameters**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





