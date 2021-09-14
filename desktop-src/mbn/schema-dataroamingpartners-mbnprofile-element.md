---
description: Spécifie la liste des fournisseurs de réseau préférés au moment de l’itinérance.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Élément DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118094"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>Élément DataRoamingPartners (MBNProfile)

L’élément **DataRoamingPartners (MBNProfile)** spécifie la liste des fournisseurs de réseau préférés au moment de l’itinérance.

Le service haut débit mobile utilise cet élément pour sélectionner le réseau préféré fourni lors de l’itinérance.

L’élément possède l’élément enfant suivant, qui doit être défini au moins une fois, mais peut être défini plusieurs fois.

-   [**Fournisseur**](schema-provider-dataroamingpartners-element.md)

Cet élément peut avoir au maximum une occurrence.

Cet élément est facultatif.

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **DataRoamingPartners** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Type                                                    | Description                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**Fournisseur**](schema-provider-dataroamingpartners-element.md) | [**providerType**](schema-providertype-complextype.md) | Nom et ID de fournisseur d’un réseau cellulaire.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




