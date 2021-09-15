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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413704"
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

 

 




