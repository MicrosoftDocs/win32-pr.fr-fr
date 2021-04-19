---
description: Pour tirer parti des fonctions IPv6 activées, les administrateurs informatiques doivent définir au sein de leur script WPAD, une fonction appelée FindProxyForURLEx (URL, hôte) qui remplacera la fonction FindProxyForUrl (URL, hôte) héritée.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: Définitions de l’API d’assistance du proxy IPv6-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528306"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="0f3a7-103">Définitions de l’API d’assistance du proxy IPv6-Aware</span><span class="sxs-lookup"><span data-stu-id="0f3a7-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="0f3a7-104">Pour tirer parti des fonctions IPv6 activées, les administrateurs informatiques doivent définir au sein de leur script WPAD, une fonction appelée FindProxyForURLEx (URL, hôte) qui remplacera la fonction FindProxyForUrl (URL, hôte) héritée.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="0f3a7-105">Les administrateurs ne peuvent exécuter les nouvelles fonctions qu’à partir de la nouvelle fonction FindProxyForURLEx.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="0f3a7-106">Nous avons également tenté de simplifier le travail pour les développeurs, en alignant nos fonctions pour qu’elles retournent différents types d’adresses IP dans le même ordre de préférence que les autres composants de mise en réseau, en particulier les adresses IPv6 suivies des adresses IPv4 (c’est-à-dire le comportement actuel de la fonction getaddrinfo (..) de Winsock).</span><span class="sxs-lookup"><span data-stu-id="0f3a7-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="0f3a7-107">Les fonctions suivantes sont des extensions de la [spécification de format de fichier de configuration automatique du proxy du navigateur](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) pour permettre aux scripts WPAD de gérer des réseaux compatibles IPv6.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="0f3a7-108">Fonctions et environnement prédéfinis pour la fonction JavaScript FindProxyforURLEx</span><span class="sxs-lookup"><span data-stu-id="0f3a7-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="0f3a7-109">Conditions basées sur un nom d’hôte</span><span class="sxs-lookup"><span data-stu-id="0f3a7-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="0f3a7-110">**isResolvableEx**</span><span class="sxs-lookup"><span data-stu-id="0f3a7-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="0f3a7-111">Détermine si une chaîne d’hôte donnée peut être résolue en une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3a7-112">**isInNetEx**</span><span class="sxs-lookup"><span data-stu-id="0f3a7-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="0f3a7-113">Détermine si une adresse IP se trouve dans un sous-réseau spécifique.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="0f3a7-114">Fonctions utilitaires associées</span><span class="sxs-lookup"><span data-stu-id="0f3a7-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="0f3a7-115">**dnsResolveEx**</span><span class="sxs-lookup"><span data-stu-id="0f3a7-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="0f3a7-116">Résoudre une chaîne d’hôte en son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3a7-117">**myIPAddressEx**</span><span class="sxs-lookup"><span data-stu-id="0f3a7-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="0f3a7-118">Recherche toutes les adresses IP pour localhost.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3a7-119">**sortIpAddressList**</span><span class="sxs-lookup"><span data-stu-id="0f3a7-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="0f3a7-120">Trie une liste d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3a7-121">**getClientVersion**</span><span class="sxs-lookup"><span data-stu-id="0f3a7-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="0f3a7-122">Obtient la version du moteur de traitement WPAD.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="0f3a7-123">Cette fonctionnalité nécessite Windows Internet Explorer 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0f3a7-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



