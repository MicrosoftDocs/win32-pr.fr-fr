---
description: Résoudre une chaîne d’hôte en son adresse IP
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: dnsResolveEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0f0100367d4fad6d6e0b013e5d552f733086e6ddd5bc720779ef1fb5b65cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133222"
---
# <a name="dnsresolveex-function"></a>dnsResolveEx fonction)

Résoudre une chaîne d’hôte en son adresse IP

## <a name="parameters"></a>Paramètres

<dl> <dt>

*host* 
</dt> <dd>

Chaîne contenant l’hôte HTTP fourni à FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne délimitée par des points-virgules contenant des adresses IPv6 et IPv4 ou une chaîne vide si l’hôte ne peut pas être résolu.

## <a name="remarks"></a>Remarques

Les implémenteurs FindProxyforURLEx doivent ajouter du code qui divise la chaîne d’adresses IP séparées par un point-virgule en adresses distinctes.

## <a name="examples"></a>Exemples

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définitions d’API d’assistance du proxy compatibles IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensions IPv6 du format de fichier de configuration automatique du navigateur](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



