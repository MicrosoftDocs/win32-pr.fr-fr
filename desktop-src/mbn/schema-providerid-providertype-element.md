---
description: Spécifie l’ID du fournisseur du réseau cellulaire.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID (providerType), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201535"
---
# <a name="providerid-providertype-element"></a>ProviderID (providerType), élément

L’élément **ProviderID (ProviderType)** spécifie l’ID du fournisseur du réseau cellulaire.

L’élément est une séquence de chiffres avec un maximum de 6 chiffres.

Cet élément est obligatoire dans l’élément [**Provider**](schema-provider-dataroamingpartners-element.md) .

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

L’élément **ProviderID** est défini par le type complexe [**ProviderType**](schema-providertype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**providerType**](schema-providertype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Fournisseur (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




