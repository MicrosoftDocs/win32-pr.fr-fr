---
description: Contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.
ms.assetid: b78cb095-a1da-4b1b-91d3-c5085325be05
title: Élément profileList (WLANPolicy)
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
ms.openlocfilehash: 9c11fbeb41b43faa31b170dcc856bb0823631001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520718"
---
# <a name="profilelist-wlanpolicy-element"></a>Élément profileList (WLANPolicy)

L’élément profileList (WLANPolicy) contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur. Cet élément est facultatif. Si cet élément est présent, il doit contenir au moins un profil.

Les profils doivent être basés sur [le \_ schéma de profil WLAN](wlan-profileschema-schema.md), avec un élément racine [**WLANProfile**](wlan-profileschema-wlanprofile-element.md).

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

L’élément **profileList** est défini par l’élément [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




