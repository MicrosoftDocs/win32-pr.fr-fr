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
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534069"
---
# <a name="isresolvableex-function"></a><span data-ttu-id="2934d-103">isResolvableEx fonction)</span><span class="sxs-lookup"><span data-stu-id="2934d-103">isResolvableEx function</span></span>

<span data-ttu-id="2934d-104">Détermine si une chaîne d’hôte donnée peut être résolue en une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="2934d-104">Determines if a given host string can resolve to an IP address.</span></span>

## <a name="parameters"></a><span data-ttu-id="2934d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2934d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2934d-106">*host*</span><span class="sxs-lookup"><span data-stu-id="2934d-106">*host*</span></span> 
</dt> <dd>

<span data-ttu-id="2934d-107">Chaîne contenant l’hôte HTTP fourni à FindProxyForUrl.</span><span class="sxs-lookup"><span data-stu-id="2934d-107">A string containing the HTTP host that is supplied to FindProxyForUrl.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2934d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2934d-108">Return value</span></span>

<span data-ttu-id="2934d-109">TRUE si l’hôte peut être résolu en une adresse IPv4 ou IPv6 ; Sinon, FALSe.</span><span class="sxs-lookup"><span data-stu-id="2934d-109">TRUE if the host is resolvable to a IPv4 or IPv6 address; otherwise, FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="2934d-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="2934d-110">Examples</span></span>

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a><span data-ttu-id="2934d-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2934d-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2934d-112">Définitions d’API d’assistance du proxy compatibles IPv6</span><span class="sxs-lookup"><span data-stu-id="2934d-112">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="2934d-113">Extensions IPv6 du format de fichier de configuration automatique du navigateur</span><span class="sxs-lookup"><span data-stu-id="2934d-113">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



