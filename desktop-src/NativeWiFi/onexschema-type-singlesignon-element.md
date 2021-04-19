---
description: Spécifie quand l’authentification unique est effectuée.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Élément type (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517540"
---
# <a name="type-singlesignon-element"></a>Élément type (singleSignOn)

L’élément type (singleSignOn) spécifie quand l’authentification unique est effectuée. Lorsque la valeur `preLogon` est définie sur, l’authentification unique est effectuée avant que l’utilisateur ouvre une session. Lorsque la valeur `postLogon` est définie sur, l’authentification unique est effectuée immédiatement après la connexion de l’utilisateur.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **type** est défini par l’élément [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




