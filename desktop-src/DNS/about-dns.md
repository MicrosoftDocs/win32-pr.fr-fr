---
title: À propos de DNS
description: Le système DNS (Domain Name System) est un protocole standard utilisé pour localiser des ordinateurs sur un réseau basé sur IP. Les utilisateurs peuvent mémoriser les noms complets, tels que www.microsoft.com, comme les adresses basées sur les nombres, telles que composées.
ms.assetid: 3a899ba4-4338-4119-aa68-a969d196c4f5
keywords:
- À propos du système DNS (Domain Name System)
- DNS (Domain Name System), à propos de
- DNS (Domain Name System), Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98573e72db645d96c263efd479135807274c18a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104211654"
---
# <a name="about-dns"></a><span data-ttu-id="dc5a5-107">À propos de DNS</span><span class="sxs-lookup"><span data-stu-id="dc5a5-107">About DNS</span></span>

<span data-ttu-id="dc5a5-108">Le système DNS (Domain Name System) est un protocole standard utilisé pour localiser des ordinateurs sur un réseau basé sur IP.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-108">Domain Name System (DNS) is an industry-standard protocol used to locate computers on an IP-based network.</span></span> <span data-ttu-id="dc5a5-109">Les utilisateurs peuvent se souvenir de noms complets, par exemple `www.microsoft.com` plus faciles que les adresses basées sur les nombres, tels que composées.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-109">Users can remember display names, such as `www.microsoft.com` easier than number-based addresses, such as 207.46.131.137.</span></span>

<span data-ttu-id="dc5a5-110">Les réseaux IP, tels que les réseaux Internet et Windows, s’appuient sur des adresses basées sur des nombres pour transmettre des données à travers le réseau. par conséquent, il est nécessaire de traduire les noms d’affichage (tels que `www.microsoft.com` ) en adresses numériques que le réseau peut reconnaître (par exemple, composées).</span><span class="sxs-lookup"><span data-stu-id="dc5a5-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to transmit data throughout the network; therefore, it is necessary to translate display names (such as `www.microsoft.com`) into numeric addresses that the network can recognize (such as 207.46.131.137).</span></span> <span data-ttu-id="dc5a5-111">DNS est le service de choix de Windows pour localiser ces ressources et les traduire en adresses IP.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-111">DNS is the service of choice in Windows to locate such resources and translate them into IP addresses.</span></span>

<span data-ttu-id="dc5a5-112">DNS est le service de localisation principal pour Active Directory. par conséquent, DNS peut être considéré comme un service de base pour Windows et Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-112">DNS is the primary locator service for Active Directory, and therefore, DNS can be considered a base service for both Windows and Active Directory.</span></span> <span data-ttu-id="dc5a5-113">Windows fournit des fonctions qui permettent aux programmeurs d’applications d’utiliser des fonctions DNS telles que la création de requêtes DNS par programmation, la comparaison d’enregistrements et la recherche de noms.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-113">Windows provides functions that enable application programmers to use DNS functions such as programmatically making DNS queries, comparing records, and looking up names.</span></span>

<span data-ttu-id="dc5a5-114">De nombreuses fonctions DNS sont en fait des types de fonction, car il existe un nom de base pour la fonction, mais son utilisation dépend de l’encodage des caractères.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-114">Many DNS functions are actually function types, in that there is a base name for the function, but its use depends on character encoding.</span></span> <span data-ttu-id="dc5a5-115">Par exemple, la fonction [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) est indiquée dans la référence de fonction de l’interface de programmation d’applications (API) DNS en tant que **DNSQuery**, toutefois, son utilisation dans les applications varie selon que l’encodage de caractères est ANSI (désigné par l’ajout \_ d’un au nom du type de fonction), Unicode (désigné par l’ajout de \_ W au nom du type de fonction) ou UTF-8 (désigné par \_ l’ajout de UTF au nom du type de fonction).</span><span class="sxs-lookup"><span data-stu-id="dc5a5-115">For example, the [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) function is listed in the function reference of the DNS Application Programming Interface (API) as **DnsQuery**, but its use in applications depends on whether the character encoding is ANSI (designated by appending \_A to the function type name), Unicode (designated by appending \_W to the function type name), or UTF-8 (designated by appending \_UTF to the function type name).</span></span> <span data-ttu-id="dc5a5-116">Par conséquent, l’appel de fonction pour la fonction **DNSQuery** serait en fait l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="dc5a5-116">Therefore, the function call for the **DnsQuery** function would actually be one of the following:</span></span>

<span data-ttu-id="dc5a5-117">DnsQuery \_ a ( \_ codage ANSI)</span><span class="sxs-lookup"><span data-stu-id="dc5a5-117">DnsQuery\_A (\_A for ANSI encoding)</span></span>

<span data-ttu-id="dc5a5-118">DnsQuery \_ w ( \_ w pour l’encodage Unicode)</span><span class="sxs-lookup"><span data-stu-id="dc5a5-118">DnsQuery\_W (\_W for Unicode encoding)</span></span>

<span data-ttu-id="dc5a5-119">DnsQuery \_ UTF8 ( \_ UTF8 pour l’encodage UTF-8)</span><span class="sxs-lookup"><span data-stu-id="dc5a5-119">DnsQuery\_UTF8 (\_UTF8 for UTF-8 encoding)</span></span>

<span data-ttu-id="dc5a5-120">Toutes les fonctions qui requièrent cette Convention indiquent clairement cette exigence dans les premières phrases de leur définition de fonction.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-120">All functions that require this convention clearly state this requirement within the first few sentences of their function definition.</span></span> <span data-ttu-id="dc5a5-121">Utilisez le nom de fonction approprié ; par exemple, vous ne pouvez pas simplement appeler [**DNSQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) au lieu de DNSQuery \_ A.</span><span class="sxs-lookup"><span data-stu-id="dc5a5-121">Use the proper function name; for example, you cannot simply call [**DnsQuery**](/windows/desktop/api/Windns/nf-windns-dnsquery_a) instead of DnsQuery\_A.</span></span>

 

 




