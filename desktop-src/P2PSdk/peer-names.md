---
description: Les noms d’homologues sont utilisés par le protocole PNRP (Peer Name Resolution Protocol), le gestionnaire d’identité homologue et l’infrastructure de regroupement d’homologues.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Noms de pairs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524226"
---
# <a name="peer-names"></a><span data-ttu-id="832c8-103">Noms de pairs</span><span class="sxs-lookup"><span data-stu-id="832c8-103">Peer Names</span></span>

<span data-ttu-id="832c8-104">Les noms d’homologues sont utilisés par le protocole PNRP (Peer Name Resolution Protocol), le gestionnaire d’identité homologue et l’infrastructure de regroupement d’homologues.</span><span class="sxs-lookup"><span data-stu-id="832c8-104">Peer names are used by Peer Name Resolution Protocol (PNRP), the Peer Identity Manager, and the Peer Grouping Infrastructure.</span></span> <span data-ttu-id="832c8-105">Les noms d’homologues sont des noms stables pour les ressources telles que les ordinateurs, les utilisateurs, les groupes ou les services.</span><span class="sxs-lookup"><span data-stu-id="832c8-105">Peer names are stable names for resources such as computers, users, groups, or services.</span></span> <span data-ttu-id="832c8-106">PNRP utilise des noms d’homologues pour identifier les nœuds d’un réseau pair à pair.</span><span class="sxs-lookup"><span data-stu-id="832c8-106">PNRP uses peer names to identify nodes in a peer network.</span></span>

> [!Note]  
> <span data-ttu-id="832c8-107">Un point de terminaison utilisé par l’infrastructure homologue est en fait un tuple qui se compose d’une adresse IPv4 ou IPv6, d’un port et d’un protocole (TCP ou UDP).</span><span class="sxs-lookup"><span data-stu-id="832c8-107">An endpoint that the Peer Infrastructure uses is actually a tuple that consists of an IPv4 or IPv6 address, port, and protocol (either TCP or UDP).</span></span> <span data-ttu-id="832c8-108">Un nom d’homologue peut avoir plusieurs tuples.</span><span class="sxs-lookup"><span data-stu-id="832c8-108">One peer name can have more than one tuple.</span></span>

 

<span data-ttu-id="832c8-109">Un nom d’homologue est une chaîne de texte au format suivant :</span><span class="sxs-lookup"><span data-stu-id="832c8-109">A peer name is a text string that has the following format:</span></span>

-   <span data-ttu-id="832c8-110">« Authority. classifier »</span><span class="sxs-lookup"><span data-stu-id="832c8-110">"Authority.Classifier"</span></span>

<span data-ttu-id="832c8-111">La valeur d’une autorité varie selon que le nom est sécurisé ou non.</span><span class="sxs-lookup"><span data-stu-id="832c8-111">The value of an Authority depends on whether the name is secure or unsecured.</span></span> <span data-ttu-id="832c8-112">Le classifieur d’un nom d’homologue est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="832c8-112">The Classifier of a peer name is a string.</span></span> <span data-ttu-id="832c8-113">Un classifieur peut être n’importe quel nom qui contient 150 caractères UNICODE ou moins.</span><span class="sxs-lookup"><span data-stu-id="832c8-113">A Classifier can be any name that contains 150 or less UNICODE characters.</span></span> <span data-ttu-id="832c8-114">Les noms d’homologues sont sensibles à la casse et peuvent être inscrits comme sécurisés ou non sécurisés.</span><span class="sxs-lookup"><span data-stu-id="832c8-114">Peer names are case-sensitive and can be registered as secured or unsecured.</span></span> <span data-ttu-id="832c8-115">La liste suivante répertorie quelques exemples de noms d’homologues :</span><span class="sxs-lookup"><span data-stu-id="832c8-115">The following list identifies some examples of peer names:</span></span>

-   <span data-ttu-id="832c8-116">« 0. MyUnsecuredPeerName »</span><span class="sxs-lookup"><span data-stu-id="832c8-116">"0.MyUnsecuredPeerName"</span></span>
-   <span data-ttu-id="832c8-117">« 0. JohnDoe. Games »</span><span class="sxs-lookup"><span data-stu-id="832c8-117">"0.JohnDoe.Games"</span></span>
-   <span data-ttu-id="832c8-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d. JohnDoe</span><span class="sxs-lookup"><span data-stu-id="832c8-118">"6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe"</span></span>

## <a name="secure-peer-names"></a><span data-ttu-id="832c8-119">Noms d’homologues sécurisés</span><span class="sxs-lookup"><span data-stu-id="832c8-119">Secure Peer Names</span></span>

<span data-ttu-id="832c8-120">Pour un nom sécurisé, l’autorité est le hachage SHA (Secure Hash Algorithm) de la clé publique du nom d’homologue et génère une chaîne hexadécimale de 40 caractères.</span><span class="sxs-lookup"><span data-stu-id="832c8-120">For a secure name, the Authority is the Secure Hash Algorithm (SHA) hash of the public key of the peer name, and results in a 40 character hexadecimal string.</span></span> <span data-ttu-id="832c8-121">Un nom d’homologue sécurisé peut uniquement être inscrit avec PNRP par le propriétaire ou le délégué du propriétaire du nom d’homologue.</span><span class="sxs-lookup"><span data-stu-id="832c8-121">A secure peer name can only be registered with PNRP by the owner or delegate of the peer name owner.</span></span> <span data-ttu-id="832c8-122">Un nom d’homologue sécurisé doit être créé en appelant [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span><span class="sxs-lookup"><span data-stu-id="832c8-122">A secured peer name must be created by calling [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).</span></span>

## <a name="unsecured-peer-names"></a><span data-ttu-id="832c8-123">Noms d’homologues non sécurisés</span><span class="sxs-lookup"><span data-stu-id="832c8-123">Unsecured Peer Names</span></span>

<span data-ttu-id="832c8-124">Pour un nom non sécurisé, l’autorité est égale à zéro (0) et le classifieur est la seule partie significative du nom d’homologue, qui crée un nom d’homologue non sécurisé sans [identité](identity-manager-api.md)associée.</span><span class="sxs-lookup"><span data-stu-id="832c8-124">For an unsecured name, the Authority is zero (0), and the Classifier is the only significant part of the peer name, which creates an unsecured peer name without an associated [identity](identity-manager-api.md).</span></span> <span data-ttu-id="832c8-125">Les noms d’homologues non sécurisés sont utilisés dans l’inscription et la résolution de noms PNRP.</span><span class="sxs-lookup"><span data-stu-id="832c8-125">Unsecured peer names are used in PNRP name registration and resolution.</span></span> <span data-ttu-id="832c8-126">Les noms d’homologues non sécurisés permettent d’inscrire et de résoudre des ressources qui ne nécessitent pas de résolution de noms sécurisée.</span><span class="sxs-lookup"><span data-stu-id="832c8-126">Unsecured peer names provide a useful way to register and resolve resources that do not require secure name resolution.</span></span> <span data-ttu-id="832c8-127">Toutefois, tout nœud peut publier n’importe quel nom non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="832c8-127">However, any node can publish any unsecured name.</span></span> <span data-ttu-id="832c8-128">Les applications concernées par la sécurité doivent s’assurer qu’elles sont robustes et sécurisées dans leur consommation de noms d’homologues non sécurisés.</span><span class="sxs-lookup"><span data-stu-id="832c8-128">Applications concerned with security must ensure that they are robust and secure in their consumption of unsecured peer names.</span></span>

> [!Note]  
> <span data-ttu-id="832c8-129">Tout le monde peut inscrire un nom d’homologue non sécurisé avec PNRP.</span><span class="sxs-lookup"><span data-stu-id="832c8-129">Anyone can register an unsecured peer name with PNRP.</span></span>

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a><span data-ttu-id="832c8-130">PNRP et l’instance de nom d’homologue la plus proche</span><span class="sxs-lookup"><span data-stu-id="832c8-130">PNRP and the Nearest Peer Name Instance</span></span>

<span data-ttu-id="832c8-131">Il peut y avoir plusieurs instances d’un nom d’homologue.</span><span class="sxs-lookup"><span data-stu-id="832c8-131">There can be more than one instance of a peer name.</span></span> <span data-ttu-id="832c8-132">Lorsque vous utilisez [PNRP](pnrp-namespace-provider-api.md) pour résoudre un nom d’homologue, il existe un concept d’instance de nom d’homologue le **plus proche** , ce qui signifie que le nom a un emplacement de service le plus proche du membre **sahint** spécifié dans [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) ou [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="832c8-132">When using [PNRP](pnrp-namespace-provider-api.md) to resolve a peer name, there is a concept of a **nearest** peer name instance, which means that the name has a service location closest to the **saHint** member specified in [**PNRPINFO\_V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) or [**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)).</span></span> <span data-ttu-id="832c8-133">Si aucun indicateur n’est fourni, le plus proche de l’une des adresses IP locales.</span><span class="sxs-lookup"><span data-stu-id="832c8-133">If no hint is supplied, closest to one of the local IP addresses.</span></span>

 

 
