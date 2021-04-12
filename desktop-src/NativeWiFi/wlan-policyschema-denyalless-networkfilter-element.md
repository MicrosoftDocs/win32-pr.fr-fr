---
description: Spécifie si l’accès à tous les réseaux d’infrastructure est bloqué.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Élément denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201357"
---
# <a name="denyalless-networkfilter-element"></a>Élément denyAllESS (networkFilter)

L’élément denyAllESS (networkFilter) spécifie si l’accès à tous les réseaux d’infrastructure est bloqué. Lorsque **denyAllESS** a la valeur true, les machines ne peuvent pas se connecter à un réseau d’infrastructure ; dans le cas contraire, les machines peuvent se connecter à des réseaux d’infrastructure.

La valeur par défaut de cet élément est FALSe. Si **denyAllESS** n’est pas spécifié dans un profil, par défaut, les ordinateurs peuvent se connecter aux réseaux d’infrastructure.

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

L’élément **denyAllESS** est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

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

 

 




