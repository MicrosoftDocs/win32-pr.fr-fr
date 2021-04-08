---
title: Protection d’accès réseau (NAP)
description: 'Remarque : la plateforme de protection d’accès réseau n’est pas disponible à partir de la protection d’accès réseau de Windows 10 (NAP) est un ensemble de composants du système d’exploitation qui offrent une plateforme pour l’accès protégé aux réseaux privés.'
ms.assetid: f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e
keywords:
- Protection d’accès réseau (NAP)
- Protection d’accès réseau, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b99348428a867be5bf846fd40b030b844460cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672734"
---
# <a name="network-access-protection"></a><span data-ttu-id="6f6f8-105">Protection d’accès réseau (NAP)</span><span class="sxs-lookup"><span data-stu-id="6f6f8-105">Network Access Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="6f6f8-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="6f6f8-106">Purpose</span></span>

> [!Note]  
> <span data-ttu-id="6f6f8-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6f6f8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6f6f8-108">La protection d’accès réseau (NAP) est un ensemble de composants du système d’exploitation qui fournissent une plateforme pour l’accès protégé aux réseaux privés.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-108">Network Access Protection (NAP) is a set of operating system components that provide a platform for protected access to private networks.</span></span> <span data-ttu-id="6f6f8-109">La plateforme NAP offre un moyen intégré d’évaluer l’état d’intégrité du système d’un client réseau qui tente de se connecter ou de communiquer sur un réseau et de restreindre l’accès du client réseau jusqu’à ce que les conditions de la stratégie de contrôle d’intégrité soient remplies.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-109">The NAP platform provides an integrated way of evaluating the system health state of a network client that is attempting to connect to or communicate on a network and restricting the access of the network client until health policy requirements have been met.</span></span>

<span data-ttu-id="6f6f8-110">La protection NAP est une plateforme extensible qui fournit une infrastructure et un ensemble d’API permettant d’ajouter des composants qui stockent, signalent, valident et corrigent l’état d’intégrité du système d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-110">NAP is an extensible platform that provides an infrastructure and an API set for adding components that store, report, validate, and correct a computer's system health state.</span></span> <span data-ttu-id="6f6f8-111">La plateforme NAP ne fournit pas de composants pour accumuler et évaluer les attributs de l’état d’intégrité d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-111">By itself, the NAP platform does not provide components to accumulate and evaluate attributes of a computer's health state.</span></span> <span data-ttu-id="6f6f8-112">D’autres composants, appelés agents d’intégrité système (SHA) et validateurs d’intégrité du système (SHV), fournissent la validation de la stratégie réseau et la conformité de la stratégie réseau.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-112">Other components, known as system health agents (SHAs) and system health validators (SHVs), provide network policy validation and network policy compliance.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6f6f8-113">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="6f6f8-113">Where applicable</span></span>

<span data-ttu-id="6f6f8-114">La protection NAP est conçue pour être extensible.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-114">NAP is designed to be extensible.</span></span> <span data-ttu-id="6f6f8-115">Il peut interagir avec n’importe quel logiciel de fournisseur qui fournit les logiciels Sha et SHV ou qui reconnaît son ensemble d’API publié.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-115">It can interoperate with any vendor software that provides SHAs and SHVs or that recognizes its published API set.</span></span> <span data-ttu-id="6f6f8-116">La protection NAP permet de fournir une solution pour les scénarios courants suivants :</span><span class="sxs-lookup"><span data-stu-id="6f6f8-116">NAP helps provide a solution for the following common scenarios:</span></span>

-   <span data-ttu-id="6f6f8-117">Vérifiez l’intégrité et l’état des ordinateurs portables itinérants.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-117">Check the health and status of roaming laptops.</span></span>
-   <span data-ttu-id="6f6f8-118">Vérifiez l’intégrité des ordinateurs de bureau.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-118">Ensure the health of desktop computers.</span></span>
-   <span data-ttu-id="6f6f8-119">Vérifier la conformité et l’intégrité des ordinateurs des bureaux distants.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-119">Verify the compliance and health of computers in remote offices.</span></span>
-   <span data-ttu-id="6f6f8-120">Déterminez l’intégrité des ordinateurs portables visités.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-120">Determine the health of visiting laptops.</span></span>
-   <span data-ttu-id="6f6f8-121">Vérifier la conformité et l’intégrité des ordinateurs personnels non gérés.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-121">Verify the compliance and health of unmanaged home computers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6f6f8-122">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="6f6f8-122">Developer audience</span></span>

<span data-ttu-id="6f6f8-123">L’API NAP est conçue pour les développeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-123">The NAP API is designed for C/C++ developers.</span></span> <span data-ttu-id="6f6f8-124">Pour les méthodes de contrainte de mise en conformité NAP, les programmeurs doivent être familiarisés avec les protocoles de mise en réseau et les technologies telles que RADIUS (Remote Authentication Dial-in User Service), DHCP (Dynamic Host Configuration Protocol), les réseaux privés virtuels (VPN), la norme IEEE 802.1 X pour l’accès câblé et sans fil et IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="6f6f8-124">For the NAP enforcement methods, programmers should be familiar with networking protocols and technologies such as Remote Authentication Dial-in User Service (RADIUS), Dynamic Host Configuration Protocol (DHCP), virtual private networks (VPNs), the IEEE 802.1X standard for wired and wireless access, and Internet Protocol security (IPsec).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6f6f8-125">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="6f6f8-125">Run-time requirements</span></span>

<span data-ttu-id="6f6f8-126">La plateforme NAP requiert des serveurs d’infrastructure NAP exécutant Windows Server 2008 ou version ultérieure et des clients NAP exécutant Windows XP avec Service Pack 3 (SP3), Windows Vista ou des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-126">The NAP platform requires NAP infrastructure servers running Windows Server 2008 or later and NAP clients running Windows XP with Service Pack 3 (SP3), Windows Vista, or later operating systems.</span></span> <span data-ttu-id="6f6f8-127">Pour obtenir des informations spécifiques sur les systèmes d’exploitation qui prennent en charge un élément de programmation particulier, reportez-vous aux sections exigences des API NAP dans la documentation de référence NAP.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-127">For specific information about which operating systems support a particular programming element, refer to the Requirements sections of the NAP APIs in the NAP Reference documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6f6f8-128">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="6f6f8-128">In this section</span></span>



| <span data-ttu-id="6f6f8-129">Rubrique</span><span class="sxs-lookup"><span data-stu-id="6f6f8-129">Topic</span></span>                                         | <span data-ttu-id="6f6f8-130">Description</span><span class="sxs-lookup"><span data-stu-id="6f6f8-130">Description</span></span>                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="6f6f8-131">À propos de NAP</span><span class="sxs-lookup"><span data-stu-id="6f6f8-131">About NAP</span></span>](about-nap.md)<br/>         | <span data-ttu-id="6f6f8-132">Informations générales sur l’API NAP.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-132">General information about NAP API.</span></span><br/>                                     |
| [<span data-ttu-id="6f6f8-133">Utilisation de NAP</span><span class="sxs-lookup"><span data-stu-id="6f6f8-133">Using NAP</span></span>](using-nap.md)<br/>         | <span data-ttu-id="6f6f8-134">Exemples d’utilisation de l’API NAP.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-134">Usage examples for NAP API.</span></span><br/>                                            |
| [<span data-ttu-id="6f6f8-135">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="6f6f8-135">NAP Reference</span></span>](nap-reference.md)<br/> | <span data-ttu-id="6f6f8-136">Documentation sur les interfaces NAP, les structures et les autres éléments de code.</span><span class="sxs-lookup"><span data-stu-id="6f6f8-136">Documentation for NAP interfaces, structures, and other code elements.</span></span><br/> |



 

 

 





