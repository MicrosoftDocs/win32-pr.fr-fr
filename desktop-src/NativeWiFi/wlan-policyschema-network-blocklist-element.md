---
description: Définit un réseau bloqué.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Élément de réseau (de blocage)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541998"
---
# <a name="network-blocklist-element"></a>Élément de réseau (de blocage)

L’élément réseau (de blocage) définit un réseau bloqué. Un ordinateur ne peut pas se connecter à un réseau bloqué.

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

L’élément **réseau** est défini [**par l’élément de la**](wlan-policyschema-blocklist-networkfilter-element.md) en-dessus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**Noires**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Blocage (networkFilter)**](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




