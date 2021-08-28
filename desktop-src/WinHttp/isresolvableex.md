---
description: Détermine si une chaîne d’hôte donnée peut être résolue en une adresse IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 580f5400b59a1142de90843e2be26790aef25a9311f7aa6f732aebeef606c701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899169"
---
# <a name="isresolvableex-function"></a>isResolvableEx fonction)

Détermine si une chaîne d’hôte donnée peut être résolue en une adresse IP.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*host* 
</dt> <dd>

Chaîne contenant l’hôte HTTP fourni à FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

TRUE si l’hôte peut être résolu en une adresse IPv4 ou IPv6 ; Sinon, FALSe.

## <a name="examples"></a>Exemples

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définitions d’API d’assistance du proxy compatibles IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensions IPv6 du format de fichier de configuration automatique du navigateur](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



