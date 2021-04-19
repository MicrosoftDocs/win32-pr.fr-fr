---
description: Détermine si une adresse IP se trouve dans un sous-réseau spécifique.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: isInNetEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: d738fbf5788fbe56d8c801b6c5256e96e8d4a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536405"
---
# <a name="isinnetex-function"></a><span data-ttu-id="57b4f-103">isInNetEx fonction)</span><span class="sxs-lookup"><span data-stu-id="57b4f-103">isInNetEx function</span></span>

<span data-ttu-id="57b4f-104">Détermine si une adresse IP se trouve dans un sous-réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="57b4f-104">Determines if an IP address is in a specific subnet.</span></span>

## <a name="parameters"></a><span data-ttu-id="57b4f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57b4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b4f-106">*IPaddress*</span><span class="sxs-lookup"><span data-stu-id="57b4f-106">*IPaddress*</span></span> 
</dt> <dd>

<span data-ttu-id="57b4f-107">Chaîne contenant des adresses IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="57b4f-107">A string containing IPv6/IPv4 addresses.</span></span>

</dd> <dt>

<span data-ttu-id="57b4f-108">*IPprefix*</span><span class="sxs-lookup"><span data-stu-id="57b4f-108">*IPprefix*</span></span> 
</dt> <dd>

<span data-ttu-id="57b4f-109">Chaîne contenant le préfixe IP délimité par des points-virgules avec les n premiers bits spécifiés dans le champ de bits (par exemple, 3FFE : 8311 : FFFF ::/48 ou 123.112.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="57b4f-109">A string containing colon delimited IP prefix with top n bits specified in the bit field (i.e. 3ffe:8311:ffff::/48 or 123.112.0.0/16).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b4f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57b4f-110">Return value</span></span>

<span data-ttu-id="57b4f-111">TRUE si l’hôte se trouve dans le même sous-réseau ; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="57b4f-111">TRUE if the host is in the same subnet; otherwise, FALSE.</span></span>

<span data-ttu-id="57b4f-112">Retourne également FALSe si le préfixe n’est pas au format approprié ou si des adresses et des préfixes de différents types sont utilisés dans la comparaison (par exemple, préfixe IPv4 et une adresse IPv6).</span><span class="sxs-lookup"><span data-stu-id="57b4f-112">Also returns FALSE if the prefix is not in the correct format or if addresses and prefixes of different types are used in the comparison (i.e. IPv4 prefix and an IPv6 address).</span></span>

## <a name="examples"></a><span data-ttu-id="57b4f-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="57b4f-113">Examples</span></span>

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a><span data-ttu-id="57b4f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57b4f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b4f-115">Définitions d’API d’assistance du proxy compatibles IPv6</span><span class="sxs-lookup"><span data-stu-id="57b4f-115">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="57b4f-116">Extensions IPv6 du format de fichier de configuration automatique du navigateur</span><span class="sxs-lookup"><span data-stu-id="57b4f-116">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



