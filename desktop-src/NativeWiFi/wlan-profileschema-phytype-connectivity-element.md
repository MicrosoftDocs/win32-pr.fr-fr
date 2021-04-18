---
description: Spécifie la norme de réseau local sans fil 802,11 utilisée sur un réseau local sans fil.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Élément phyType (Connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519275"
---
# <a name="phytype-connectivity-element"></a>Élément phyType (Connectivity)

L’élément phyType (Connectivity) spécifie la norme de réseau local sans fil 802,11 utilisée sur un réseau local sans fil.

Vous pouvez spécifier plusieurs **phyType** s. Si aucun **phyType** n’est spécifié, le profil peut être utilisé pour se connecter à n’importe quel **phyType**. La valeur « n » est uniquement prise en charge sur Windows Vista avec Service Pack 1 (SP1) et les versions ultérieures du système d’exploitation.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par l’élément [**Connectivity**](wlan-profileschema-connectivity-msm-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**connectivité**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**connectivité (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




