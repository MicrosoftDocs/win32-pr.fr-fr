---
title: Modèle objet
description: Le tableau suivant répertorie les types d’objets qui peuvent être manipulés à l’aide des divers jeux d’API fournis par la plateforme de filtrage Windows (WFP).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030848"
---
# <a name="object-model"></a><span data-ttu-id="02ea0-103">Modèle objet</span><span class="sxs-lookup"><span data-stu-id="02ea0-103">Object Model</span></span>

<span data-ttu-id="02ea0-104">Le tableau suivant répertorie les types d’objets qui peuvent être manipulés à l’aide des divers jeux d’API fournis par la plateforme de filtrage Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="02ea0-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02ea0-105">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="02ea0-105">Object Type</span></span></th>
<th><span data-ttu-id="02ea0-106">Description</span><span class="sxs-lookup"><span data-stu-id="02ea0-106">Description</span></span></th>
<th><span data-ttu-id="02ea0-107">Exemples de propriétés</span><span class="sxs-lookup"><span data-stu-id="02ea0-107">Sample Properties</span></span></th>
<th><span data-ttu-id="02ea0-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="02ea0-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02ea0-109">Filtrer</span><span class="sxs-lookup"><span data-stu-id="02ea0-109">Filter</span></span></td>
<td><span data-ttu-id="02ea0-110">Règle qui régit la classification.</span><span class="sxs-lookup"><span data-stu-id="02ea0-110">A rule that governs classification.</span></span> <span data-ttu-id="02ea0-111">Si les conditions sont remplies, l’action est appelée.</span><span class="sxs-lookup"><span data-stu-id="02ea0-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="02ea0-112">Il s’agit de l’objet le plus complexe exposé par WFP, car il associe tous les autres types d’objets.</span><span class="sxs-lookup"><span data-stu-id="02ea0-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="02ea0-113">Tableau de conditions</span><span class="sxs-lookup"><span data-stu-id="02ea0-113">Array of conditions</span></span></li>
<li><span data-ttu-id="02ea0-114">Action (autorisation, bloc, légende)</span><span class="sxs-lookup"><span data-stu-id="02ea0-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="02ea0-115"><a href="filter-weight-assignment.md">Poids</a></span><span class="sxs-lookup"><span data-stu-id="02ea0-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="02ea0-116">Context</span><span class="sxs-lookup"><span data-stu-id="02ea0-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="02ea0-117">&quot;Bloquez le trafic avec un port TCP supérieur à 1024.&quot;</span><span class="sxs-lookup"><span data-stu-id="02ea0-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="02ea0-118">&quot;Appel à des ID pour tout le trafic qui n’est pas sécurisé.&quot;</span><span class="sxs-lookup"><span data-stu-id="02ea0-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02ea0-119">Légende</span><span class="sxs-lookup"><span data-stu-id="02ea0-119">Callout</span></span></td>
<td><span data-ttu-id="02ea0-120">Ensemble de fonctions qui participent au processus de classification.</span><span class="sxs-lookup"><span data-stu-id="02ea0-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="02ea0-121">Cela permet d’effectuer un traitement personnalisé des paquets lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="02ea0-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="02ea0-122">id</span><span class="sxs-lookup"><span data-stu-id="02ea0-122">ID</span></span></li>
<li><span data-ttu-id="02ea0-123">Couche applicable</span><span class="sxs-lookup"><span data-stu-id="02ea0-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="02ea0-124">Le pilote NAT</span><span class="sxs-lookup"><span data-stu-id="02ea0-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02ea0-125">Couche</span><span class="sxs-lookup"><span data-stu-id="02ea0-125">Layer</span></span></td>
<td><span data-ttu-id="02ea0-126">Conteneur de filtre dans le moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="02ea0-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="02ea0-127">Représente un point spécifique dans le traitement du trafic réseau où le moteur de filtre est appelé.</span><span class="sxs-lookup"><span data-stu-id="02ea0-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="02ea0-128">Schéma pour les filtres qui peuvent être ajoutés à la couche</span><span class="sxs-lookup"><span data-stu-id="02ea0-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="02ea0-129">Couche de transport entrante</span><span class="sxs-lookup"><span data-stu-id="02ea0-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02ea0-130">Sous-couche</span><span class="sxs-lookup"><span data-stu-id="02ea0-130">Sub-layer</span></span></td>
<td><span data-ttu-id="02ea0-131">Sous-composant d’une couche, utilisé dans un <a href="filter-arbitration.md">arbitrage de filtre</a>.</span><span class="sxs-lookup"><span data-stu-id="02ea0-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="02ea0-132">Poids</span><span class="sxs-lookup"><span data-stu-id="02ea0-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="02ea0-133">Sous-couche du tunnel IPsec</span><span class="sxs-lookup"><span data-stu-id="02ea0-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02ea0-134">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="02ea0-134">Provider</span></span></td>
<td><span data-ttu-id="02ea0-135">Un fournisseur de stratégie qui a créé une solution sur WFP.</span><span class="sxs-lookup"><span data-stu-id="02ea0-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="02ea0-136">Il est utilisé uniquement à des fins de gestion ; elle n’affecte pas le traitement des paquets au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="02ea0-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="02ea0-137">id</span><span class="sxs-lookup"><span data-stu-id="02ea0-137">ID</span></span></li>
<li><span data-ttu-id="02ea0-138">Nom du service</span><span class="sxs-lookup"><span data-stu-id="02ea0-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="02ea0-139">Pare-feu Windows avec fonctions avancées de sécurité</span><span class="sxs-lookup"><span data-stu-id="02ea0-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="02ea0-140">Application tierce de filtrage d’URL</span><span class="sxs-lookup"><span data-stu-id="02ea0-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02ea0-141">Contexte du fournisseur</span><span class="sxs-lookup"><span data-stu-id="02ea0-141">Provider Context</span></span></td>
<td><span data-ttu-id="02ea0-142">Objet blob de données utilisé par un fournisseur de stratégie pour stocker des informations de contexte arbitraires.</span><span class="sxs-lookup"><span data-stu-id="02ea0-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="02ea0-143">Il est utilisé pour passer des informations de configuration personnalisées à une légende.</span><span class="sxs-lookup"><span data-stu-id="02ea0-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="02ea0-144">La façon la plus courante d’utiliser les informations de contexte est d’avoir des filtres qui référencent un contexte de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02ea0-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="02ea0-145">id</span><span class="sxs-lookup"><span data-stu-id="02ea0-145">ID</span></span></li>
<li><span data-ttu-id="02ea0-146">Objet blob de données</span><span class="sxs-lookup"><span data-stu-id="02ea0-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="02ea0-147">IPsec stocke les paramètres d’authentification dans le moteur de filtrage de base (BFE).</span><span class="sxs-lookup"><span data-stu-id="02ea0-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="02ea0-148">La &quot; &quot; propriété de contexte d’un filtre indique les paramètres d’authentification à utiliser pour le trafic décrit par le filtre.</span><span class="sxs-lookup"><span data-stu-id="02ea0-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="02ea0-149">Le shim de sélection de certification SSL stocke les informations de certification dans un contexte de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02ea0-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="02ea0-150">Les types d’objets exposés par l’API WFP ont une sémantique cohérente.</span><span class="sxs-lookup"><span data-stu-id="02ea0-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="02ea0-151">Les actions d’ajout, d’énumération, d’abonnement, etc. sont similaires pour tous les types d’objets.</span><span class="sxs-lookup"><span data-stu-id="02ea0-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="02ea0-152">Chaque type d’objet est représenté par une structure de données (par exemple, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span><span class="sxs-lookup"><span data-stu-id="02ea0-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="02ea0-153">Afin de réduire le nombre de structures de données différentes exposées par l’API WFP, la même structure de données est utilisée pour l’ajout de nouveaux objets et la récupération de ceux existants.</span><span class="sxs-lookup"><span data-stu-id="02ea0-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="02ea0-154">Par conséquent, il peut y avoir des champs dans chaque structure de données qui sont ignorés lors de l’ajout d’un nouvel objet, car ces champs sont renseignés par le moteur de filtrage de base (BFE) et non par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="02ea0-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="02ea0-155">Par exemple, une structure de données **FWPM \_ FILTER0** a un champ **FilterId** qui contient le **LUID** du **\_ FILTER0 FWPS** correspondant.</span><span class="sxs-lookup"><span data-stu-id="02ea0-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="02ea0-156">Ce **LUID** est assigné par BFE, ce qui signifie que ce champ est ignoré dans l’appel à [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span><span class="sxs-lookup"><span data-stu-id="02ea0-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02ea0-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02ea0-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ea0-158">Gestion des objets</span><span class="sxs-lookup"><span data-stu-id="02ea0-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 





