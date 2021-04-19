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
# <a name="sortipaddresslist-function"></a><span data-ttu-id="34116-103">sortIpAddressList fonction)</span><span class="sxs-lookup"><span data-stu-id="34116-103">sortIpAddressList function</span></span>

<span data-ttu-id="34116-104">Trie une liste d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="34116-104">Sorts a list of IP addresses.</span></span>

## <a name="parameters"></a><span data-ttu-id="34116-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34116-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34116-106">*IpAddressList*</span><span class="sxs-lookup"><span data-stu-id="34116-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="34116-107">Chaîne délimitée par des points-virgules contenant des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="34116-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34116-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34116-108">Return value</span></span>

<span data-ttu-id="34116-109">Liste d’adresses IP séparées par des points-virgules triées ou une chaîne vide si le tri de la liste d’adresses IP est impossible.</span><span class="sxs-lookup"><span data-stu-id="34116-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="34116-110">Notes</span><span class="sxs-lookup"><span data-stu-id="34116-110">Remarks</span></span>

<span data-ttu-id="34116-111">Les implémenteurs FindProxyforURLEx doivent ajouter du code qui divise la chaîne d’adresses IP séparées par un point-virgule en adresses distinctes.</span><span class="sxs-lookup"><span data-stu-id="34116-111">FindProxyforURLEx implementers should add code that breaks the string of semi-colon delimited IP addresses into separate addresses.</span></span>

## <a name="examples"></a><span data-ttu-id="34116-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="34116-112">Examples</span></span>

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a><span data-ttu-id="34116-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34116-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34116-114">Définitions d’API d’assistance du proxy compatibles IPv6</span><span class="sxs-lookup"><span data-stu-id="34116-114">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="34116-115">Extensions IPv6 du format de fichier de configuration automatique du navigateur</span><span class="sxs-lookup"><span data-stu-id="34116-115">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



