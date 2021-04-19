---
description: Contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.
ms.assetid: 4f010449-0c6b-4a01-8253-4f82cd628f0a
title: Élément profileList (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- profileList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b85c284262c070f7a9349933f99ad858cf047913
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536741"
---
# <a name="profilelist-lanpolicy-element"></a>Élément profileList (LANPolicy)

L’élément profileList (LANPolicy) contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur. Les profils doivent être basés sur [le \_ schéma de profil de réseau local](lan-profileschema-schema.md), avec un élément racine [**LANProfile**](lan-profileschema-lanprofile-element.md). Les profils basés sur un autre schéma seront ignorés.

Quand [**enableAutoConfig**](lan-policyschema-enableautoconfig-globalflags-element.md) est défini sur false, cet élément ne doit pas être présent dans un profil de stratégie de réseau local. Quand **enableAutoConfig** a la valeur true, cet élément est requis.

``` syntax
<xs:element name="profileList">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **profileList** est défini par l’élément [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .

## <a name="remarks"></a>Notes

Cet élément doit contenir exactement un profil réseau. Si plusieurs profils sont spécifiés dans la stratégie, seul le premier réseau sera appliqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**LANPolicy**](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




