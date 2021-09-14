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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119394"
---
# <a name="heldperiod-onex-element"></a>Élément heldPeriod (OneX)

L’élément heldPeriod (OneX) spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.

Cet élément est facultatif. Quand heldPeriod n’est pas spécifié dans un profil, une valeur de 1 seconde est utilisée.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 




