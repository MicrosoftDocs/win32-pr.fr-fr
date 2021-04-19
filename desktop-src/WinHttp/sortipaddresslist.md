---
description: Trie une liste d’adresses IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList fonction)
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538837"
---
# <a name="sortipaddresslist-function"></a>sortIpAddressList fonction)

Trie une liste d’adresses IP.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Chaîne délimitée par des points-virgules contenant des adresses IP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Liste d’adresses IP séparées par des points-virgules triées ou une chaîne vide si le tri de la liste d’adresses IP est impossible.

## <a name="remarks"></a>Notes

Les implémenteurs FindProxyforURLEx doivent ajouter du code qui divise la chaîne d’adresses IP séparées par un point-virgule en adresses distinctes.

## <a name="examples"></a>Exemples

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définitions d’API d’assistance du proxy compatibles IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Extensions IPv6 du format de fichier de configuration automatique du navigateur](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



