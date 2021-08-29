---
description: Spécifie si la compression sera utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Élément compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 9715114bc44cebef9f342795e2c46283b8737c2478d9af9bd983deca50d3114e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959849"
---
# <a name="compression-contexttype-element"></a>Élément compression (contextType)

L’élément **compression (ContextType)** spécifie si la compression est utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données.

Cet élément peut prendre l’une des valeurs suivantes.

| Valeur     | Signification                       |
|-----------|-------------------------------|
| RENDRE  | La compression sera utilisée.     |
| DÉSACTIVE | La compression n’est pas utilisée. |



 

Cet élément est facultatif. Si cet élément n’est pas spécifié, le système haut débit mobile n’utilise pas la compression.

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **compression** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Contexte (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




