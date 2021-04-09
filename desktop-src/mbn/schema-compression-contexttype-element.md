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
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862762"
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
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
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

 

 




