---
description: Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Élément OneXEnforced (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bcaa8604fb8b813417299725133e9c6e51f7d7510b540cf8495ff9009b9d1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798439"
---
# <a name="onexenforced-security-element"></a>Élément OneXEnforced (Security)

L’élément **OneXEnforced** (Security) spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 x pour l’authentification de port. Quand **OneXEnforced** a la valeur true, le service de configuration automatique doit utiliser 802.1 x pour l’authentification de port. Quand **OneXEnforced** a la valeur false, le service de configuration automatique tente d’utiliser 802.1 x pour l’authentification de port, mais le service revient à aucune authentification si l’authentification 802.1 x échoue pour une raison quelconque.

Cet élément est facultatif. La valeur par défaut est FALSE.

Cet élément a une valeur significative uniquement si [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) a la valeur true. Si **OneXEnabled** a la valeur false, la valeur de cet élément est ignorée.

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

L’élément **OneXEnforced** est défini par l’élément de [**sécurité**](lan-profileschema-security-msm-element.md) .

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

 

 




