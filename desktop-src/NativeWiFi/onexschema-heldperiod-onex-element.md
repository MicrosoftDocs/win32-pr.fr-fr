---
description: Spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Élément heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527637"
---
# <a name="heldperiod-onex-element"></a>Élément heldPeriod (OneX)

L’élément heldPeriod (OneX) spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.

Cet élément est facultatif. Quand heldPeriod n’est pas spécifié dans un profil, une valeur de 1 seconde est utilisée.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **heldPeriod** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 




