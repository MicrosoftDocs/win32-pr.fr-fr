---
description: Contient une hexBinary de 3 octets qui identifie le IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Élément OUI (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538848"
---
# <a name="oui-ouiheader-element"></a>Élément OUI (OUIHeader)

L’élément OUI (OUIHeader) contient un élément hexBinary de 3 octets qui identifie le IHV.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par l’élément [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




