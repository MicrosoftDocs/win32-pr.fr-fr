---
description: Identifie le nom et l’ID de fournisseur d’un réseau cellulaire.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Élément Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347159"
---
# <a name="provider-dataroamingpartners-element"></a>Élément Provider (DataRoamingPartners)

L’élément **Provider (DataRoamingPartners)** identifie le nom et l’ID de fournisseur d’un réseau cellulaire.

Cet élément possède les éléments enfants suivants.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Cet élément peut être défini plusieurs fois dans l’élément [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) . Elle doit être définie au moins une fois.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

L’élément **Provider** est défini par l’élément [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




