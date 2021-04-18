---
description: L’API DRT (Distributed Routing Table) utilise les fonctions suivantes.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Fonctions de table de routage distribuée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536369"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="09058-103">Fonctions de table de routage distribuée</span><span class="sxs-lookup"><span data-stu-id="09058-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="09058-104">L’API DRT (Distributed Routing Table) utilise les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="09058-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="09058-105">Fonctions de gestion de la durée de vie</span><span class="sxs-lookup"><span data-stu-id="09058-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="09058-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="09058-106">Function</span></span>                                           | <span data-ttu-id="09058-107">Description</span><span class="sxs-lookup"><span data-stu-id="09058-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09058-108">**DrtOpen**</span><span class="sxs-lookup"><span data-stu-id="09058-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="09058-109">Crée une instance DRT locale à l’aide de critères spécifiés par la structure de [**\_ paramètres DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="09058-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="09058-110">**DrtClose**</span><span class="sxs-lookup"><span data-stu-id="09058-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="09058-111">Ferme et supprime l’instance locale de DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="09058-112">**DrtGetEventData**</span><span class="sxs-lookup"><span data-stu-id="09058-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="09058-113">Récupère les données d’événement associées à un événement signalé.</span><span class="sxs-lookup"><span data-stu-id="09058-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="09058-114">**DrtGetEventDataSize**</span><span class="sxs-lookup"><span data-stu-id="09058-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="09058-115">Retourne la taille de la structure de [**\_ \_ données d’événement DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) associée à un événement signalé.</span><span class="sxs-lookup"><span data-stu-id="09058-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="09058-116">Fonctions de gestion des modules</span><span class="sxs-lookup"><span data-stu-id="09058-116">Module Management Functions</span></span>



| <span data-ttu-id="09058-117">Fonction</span><span class="sxs-lookup"><span data-stu-id="09058-117">Function</span></span>                                                                           | <span data-ttu-id="09058-118">Description</span><span class="sxs-lookup"><span data-stu-id="09058-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09058-119">**DrtCreatePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="09058-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="09058-120">Crée un programme de résolution de démarrage basé sur le protocole PNRP.</span><span class="sxs-lookup"><span data-stu-id="09058-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="09058-121">**DrtDeletePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="09058-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="09058-122">Supprime un programme de résolution de démarrage basé sur le protocole PNRP.</span><span class="sxs-lookup"><span data-stu-id="09058-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="09058-123">**DrtCreateDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="09058-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="09058-124">Crée un fournisseur de démarrage qui contacte un hôte bien connu par son nom.</span><span class="sxs-lookup"><span data-stu-id="09058-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="09058-125">**DrtDeleteDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="09058-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="09058-126">Supprime un fournisseur de démarrage qui contacte un hôte bien connu par son nom.</span><span class="sxs-lookup"><span data-stu-id="09058-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="09058-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="09058-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="09058-128">Crée un transport basé sur le protocole UDP IPv6.</span><span class="sxs-lookup"><span data-stu-id="09058-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="09058-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="09058-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="09058-130">Supprime un transport basé sur le protocole UDP IPv6.</span><span class="sxs-lookup"><span data-stu-id="09058-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="09058-131">**DrtCreateDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="09058-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="09058-132">Crée un fournisseur de sécurité de clé dérivée pour DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="09058-133">**DrtCreateDerivedKey**</span><span class="sxs-lookup"><span data-stu-id="09058-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="09058-134">Crée une clé qui peut être utilisée par [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) lorsque DRT utilise un fournisseur de sécurité de clé dérivé.</span><span class="sxs-lookup"><span data-stu-id="09058-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="09058-135">**DrtDeleteDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="09058-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="09058-136">Supprime un fournisseur de sécurité de clé dérivé pour DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="09058-137">**DrtCreateNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="09058-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="09058-138">Crée un fournisseur de sécurité null.</span><span class="sxs-lookup"><span data-stu-id="09058-138">Creates a null security provider.</span></span> <span data-ttu-id="09058-139">Ce fournisseur de sécurité ne nécessite pas que les nœuds authentifient les clés.</span><span class="sxs-lookup"><span data-stu-id="09058-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="09058-140">**DrtDeleteNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="09058-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="09058-141">Supprime un fournisseur de sécurité null.</span><span class="sxs-lookup"><span data-stu-id="09058-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="09058-142">Fonctions d’inscription</span><span class="sxs-lookup"><span data-stu-id="09058-142">Registration Functions</span></span>



| <span data-ttu-id="09058-143">Fonction</span><span class="sxs-lookup"><span data-stu-id="09058-143">Function</span></span>                                     | <span data-ttu-id="09058-144">Description</span><span class="sxs-lookup"><span data-stu-id="09058-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="09058-145">**DrtRegisterKey**</span><span class="sxs-lookup"><span data-stu-id="09058-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="09058-146">Inscrit une clé dans DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="09058-147">**DrtUpdateKey**</span><span class="sxs-lookup"><span data-stu-id="09058-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="09058-148">Met à jour les données d’application associées à une clé inscrite.</span><span class="sxs-lookup"><span data-stu-id="09058-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="09058-149">**DrtUnregisterKey**</span><span class="sxs-lookup"><span data-stu-id="09058-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="09058-150">Annule l’inscription d’une clé de l’DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="09058-151">Fonctions de recherche</span><span class="sxs-lookup"><span data-stu-id="09058-151">Search Functions</span></span>



| <span data-ttu-id="09058-152">Fonction</span><span class="sxs-lookup"><span data-stu-id="09058-152">Function</span></span>                                                 | <span data-ttu-id="09058-153">Description</span><span class="sxs-lookup"><span data-stu-id="09058-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09058-154">**DrtStartSearch**</span><span class="sxs-lookup"><span data-stu-id="09058-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="09058-155">Recherche une clé à l’aide de critères spécifiés dans la structure d' [**\_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="09058-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="09058-156">**DrtContinueSearch**</span><span class="sxs-lookup"><span data-stu-id="09058-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="09058-157">Poursuit un \_ chemin de retour de recherche DRT \_ \_ Rechercher une clé dans le DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="09058-158">Cette fonction est utilisée uniquement lorsque l’indicateur **fIterative** est défini sur **true** dans la structure [**d' \_ \_ informations de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) associée.</span><span class="sxs-lookup"><span data-stu-id="09058-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="09058-159">**DrtGetSearchResult**</span><span class="sxs-lookup"><span data-stu-id="09058-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="09058-160">Récupère le ou les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="09058-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="09058-161">**DrtGetSearchResultSize**</span><span class="sxs-lookup"><span data-stu-id="09058-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="09058-162">Retourne la taille du résultat de la recherche disponible suivant.</span><span class="sxs-lookup"><span data-stu-id="09058-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="09058-163">**DrtGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="09058-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="09058-164">Retourne la liste des nœuds contactés pendant l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="09058-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="09058-165">**DrtGetSearchPathSize**</span><span class="sxs-lookup"><span data-stu-id="09058-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="09058-166">Retourne la taille du chemin de recherche, qui représente le nombre de nœuds utilisés dans l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="09058-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="09058-167">**DrtEndSearch**</span><span class="sxs-lookup"><span data-stu-id="09058-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="09058-168">Annule la recherche d’une clé dans un objet DRT et, par conséquent, le retour des résultats via [**le \_ \_ résultat de la recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) est arrêté.</span><span class="sxs-lookup"><span data-stu-id="09058-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="09058-169">Cette API peut être appelée à tout moment après l’émission d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="09058-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="09058-170">Fonctions de nom d’instance</span><span class="sxs-lookup"><span data-stu-id="09058-170">Instance Name Functions</span></span>



| <span data-ttu-id="09058-171">Fonction</span><span class="sxs-lookup"><span data-stu-id="09058-171">Function</span></span>                                                 | <span data-ttu-id="09058-172">Description</span><span class="sxs-lookup"><span data-stu-id="09058-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="09058-173">**DrtGetInstanceName**</span><span class="sxs-lookup"><span data-stu-id="09058-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="09058-174">Obtient le nom associé à une instance DRT.</span><span class="sxs-lookup"><span data-stu-id="09058-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="09058-175">**DrtGetInstanceNameSize**</span><span class="sxs-lookup"><span data-stu-id="09058-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="09058-176">Retourne la taille du nom de l’instance de la table de routage distribuée.</span><span class="sxs-lookup"><span data-stu-id="09058-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09058-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09058-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09058-178">Énumérations de tables de routage distribuées</span><span class="sxs-lookup"><span data-stu-id="09058-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="09058-179">Structures de table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="09058-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="09058-180">Référence de API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="09058-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



