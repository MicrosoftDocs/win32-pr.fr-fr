---
description: Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Élément OneXEnabled (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aaaf5344078e4c8da2e5ee2118eed84563ebeb4daa8aebd700a29630b2fe4301
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801089"
---
# <a name="onexenabled-security-element"></a>Élément OneXEnabled (Security)

L’élément **OneXEnabled** (sécurité) spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 x. Quand **OneXEnabled** a la valeur false, le service de configuration automatique n’utilise jamais 802.1 x pour l’authentification de port. Quand **OneXEnabled** a la valeur true, le service de configuration automatique tente l’authentification de port à l’aide de 802.1 x.

Cet élément est facultatif. La valeur par défaut est TRUE. Quand **OneXEnabled** n’est pas spécifié dans un profil, 802.1 x peut être utilisé pour l’authentification du port.

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

L’élément **OneXEnabled** est défini par l’élément de [**sécurité**](lan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**caution**](lan-profileschema-security-msm-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**sécurité (MSM)**](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




