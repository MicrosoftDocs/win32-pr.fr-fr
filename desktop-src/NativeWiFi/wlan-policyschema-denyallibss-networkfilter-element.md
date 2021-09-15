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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413703"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



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

 

 




