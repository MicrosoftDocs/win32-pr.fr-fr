---
title: Système de nom de domaine
description: DNS (Domain Name System), un service de localisation dans Microsoft Windows, est un protocole standard qui localise les ordinateurs sur un réseau IP.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS, (voir Domain Name System)
- Système de nom de domaine
- Domain Name System, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104043074"
---
# <a name="domain-name-system"></a><span data-ttu-id="7889b-107">Système de nom de domaine</span><span class="sxs-lookup"><span data-stu-id="7889b-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="7889b-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="7889b-108">Purpose</span></span>

<span data-ttu-id="7889b-109">DNS (Domain Name System), un service de localisation dans Microsoft Windows, est un protocole standard qui localise les ordinateurs sur un réseau IP.</span><span class="sxs-lookup"><span data-stu-id="7889b-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="7889b-110">Les réseaux IP, tels que les réseaux Internet et Windows, s’appuient sur des adresses basées sur des nombres pour traiter les données.</span><span class="sxs-lookup"><span data-stu-id="7889b-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="7889b-111">Toutefois, les utilisateurs peuvent plus facilement mémoriser les adresses de noms. il est donc nécessaire de traduire des noms conviviaux (tels que `www.microsoft.com` ) en adresses reconnues par le réseau (par exemple, composées).</span><span class="sxs-lookup"><span data-stu-id="7889b-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7889b-112">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="7889b-112">Where applicable</span></span>

<span data-ttu-id="7889b-113">Windows et Active Directory utilisent DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="7889b-114">DNS est le service de localisation principal pour Internet et Active Directory. par conséquent, DNS est considéré comme un service de base pour Windows et Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7889b-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7889b-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="7889b-115">Developer audience</span></span>

<span data-ttu-id="7889b-116">Windows fournit des fonctions qui permettent aux programmeurs d’applications d’utiliser DNS, tels que la requête DNS par programmation, la comparaison d’enregistrements et la recherche de noms.</span><span class="sxs-lookup"><span data-stu-id="7889b-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="7889b-117">Les composants DNS programmables sont conçus pour être utilisés par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="7889b-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="7889b-118">Vous devez être familiarisé avec la mise en réseau et DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="7889b-119">Les programmeurs doivent être familiarisés avec la suite de protocoles IP, ainsi que le protocole DNS et les opérations DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7889b-120">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="7889b-120">Run-time requirements</span></span>

<span data-ttu-id="7889b-121">DNS est utilisé sur tous les réseaux IP qui requièrent un service de localisation compatible avec Internet.</span><span class="sxs-lookup"><span data-stu-id="7889b-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="7889b-122">Toutefois, l’API DNS requiert Windows 2000 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7889b-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7889b-123">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="7889b-123">In this section</span></span>



| <span data-ttu-id="7889b-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7889b-124">Topic</span></span>                                                             | <span data-ttu-id="7889b-125">Description</span><span class="sxs-lookup"><span data-stu-id="7889b-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7889b-126">Documents de normes DNS</span><span class="sxs-lookup"><span data-stu-id="7889b-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="7889b-127">Liens vers les documents de normes DNS publics.</span><span class="sxs-lookup"><span data-stu-id="7889b-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="7889b-128">À propos de DNS</span><span class="sxs-lookup"><span data-stu-id="7889b-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="7889b-129">Informations générales sur DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="7889b-130">Référence DNS</span><span class="sxs-lookup"><span data-stu-id="7889b-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="7889b-131">Documentation de référence pour DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="7889b-132">Fournisseur WMI DNS</span><span class="sxs-lookup"><span data-stu-id="7889b-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="7889b-133">Informations générales et documentation de référence pour le fournisseur WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="7889b-134">Glossaire</span><span class="sxs-lookup"><span data-stu-id="7889b-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="7889b-135">Glossaire des termes et définitions DNS.</span><span class="sxs-lookup"><span data-stu-id="7889b-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="7889b-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7889b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7889b-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="7889b-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="7889b-138">Assistance du protocole Internet</span><span class="sxs-lookup"><span data-stu-id="7889b-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="7889b-139">[Services d’annuaire](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="7889b-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

