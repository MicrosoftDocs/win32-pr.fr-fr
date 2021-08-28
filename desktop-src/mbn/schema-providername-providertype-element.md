---
description: Contient le nom du réseau cellulaire.
ms.assetid: 4169babb-7616-468a-93f0-de25cce0c88b
title: Élément ProviderName (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderName
api_type:
- Schema
ms.openlocfilehash: 6d5e6bd95c5bea00cec90f27658c41e7f1a3a99f8ddce6870c60f54e9eaf1717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975148"
---
# <a name="providername-providertype-element"></a>Élément ProviderName (providerType)

L’élément **providerName (ProviderType)** contient le nom du réseau cellulaire.

L’élément est une chaîne comportant un maximum de 20 caractères.

Cet élément est facultatif.

``` syntax
<xs:element name="ProviderName"
    type="providerNameType"
 />
```

L’élément **providerName** est défini par le type complexe [**ProviderType**](schema-providertype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
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

 

 




