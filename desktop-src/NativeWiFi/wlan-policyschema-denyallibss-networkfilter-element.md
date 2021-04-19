---
description: Spécifie si l’accès à tous les réseaux ad hoc est bloqué.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Élément denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514414"
---
# <a name="denyallibss-networkfilter-element"></a>Élément denyAllIBSS (networkFilter)

L’élément denyAllIBSS (networkFilter) spécifie si l’accès à tous les réseaux ad hoc est bloqué. Lorsque **denyAllIBSS** a la valeur true, les machines ne peuvent pas se connecter à un réseau ad hoc. dans le cas contraire, les machines peuvent se connecter à des réseaux ad hoc.

La valeur par défaut de cet élément est FALSe. Si **denyAllIBSS** n’est pas spécifié dans un profil, par défaut, les ordinateurs peuvent se connecter à des réseaux ad hoc.

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

L’élément **denyAllIBSS** est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




