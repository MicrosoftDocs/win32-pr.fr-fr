---
title: Traitement des groupes et des rappels
description: Le tableau suivant résume une série d’étapes dans une interaction opérationnelle entre un protocole de routage et le gestionnaire de groupe de multidiffusion.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316637"
---
# <a name="processing-groups-and-callbacks"></a><span data-ttu-id="20c52-103">Traitement des groupes et des rappels</span><span class="sxs-lookup"><span data-stu-id="20c52-103">Processing Groups and Callbacks</span></span>

<span data-ttu-id="20c52-104">Le tableau suivant résume une série d’étapes dans une interaction opérationnelle entre un protocole de routage et le gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="20c52-104">The following table summarizes a series of steps in an operational interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="20c52-105">La première colonne décrit les actions effectuées par le protocole de routage et les réponses du protocole de routage au gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="20c52-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="20c52-106">La deuxième colonne décrit les réponses du gestionnaire de groupe de multidiffusion au protocole de routage et toutes les actions effectuées par le gestionnaire de groupe de multidiffusion, telles que les rappels.</span><span class="sxs-lookup"><span data-stu-id="20c52-106">The second column describes the multicast group manager's responses to the routing protocol and any actions the multicast group manager performs such as callbacks.</span></span> <span data-ttu-id="20c52-107">La troisième colonne présente des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="20c52-107">The third column presents any additional information.</span></span>

<span data-ttu-id="20c52-108">Chaque ligne de la table représente une étape.</span><span class="sxs-lookup"><span data-stu-id="20c52-108">Each row of the table represents one step.</span></span>

<span data-ttu-id="20c52-109">Les tâches listées dans ce tableau ne se produisent pas dans un ordre spécifique. au lieu de cela, ils se produisent en fonction de l’état des appartenances aux groupes de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="20c52-109">The tasks listed in this table do not occur in any specific order; rather, they occur based on the status of multicast group memberships.</span></span> <span data-ttu-id="20c52-110">Le tableau ci-dessous montre un exemple d’ordre.</span><span class="sxs-lookup"><span data-stu-id="20c52-110">The table below shows an example order.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20c52-111">Action de protocole de routage</span><span class="sxs-lookup"><span data-stu-id="20c52-111">Routing protocol action</span></span></th>
<th><span data-ttu-id="20c52-112">Action du gestionnaire de groupe de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="20c52-112">Multicast group manager action</span></span></th>
<th><span data-ttu-id="20c52-113">Notes</span><span class="sxs-lookup"><span data-stu-id="20c52-113">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20c52-114">Gérer les appartenances aux groupes en fonction des informations de protocole reçues sur les interfaces que le protocole possède.</span><span class="sxs-lookup"><span data-stu-id="20c52-114">Manage group memberships based on protocol information received on those interfaces that the protocol owns.</span></span> <span data-ttu-id="20c52-115">La gestion s’effectue à l’aide des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="20c52-115">Management is performed using the following functions:</span></span>
<ul>
<li><span data-ttu-id="20c52-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="20c52-116"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></span></span></li>
<li><span data-ttu-id="20c52-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="20c52-117"><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="20c52-118">Ajoutez et supprimez dans la liste des interfaces sortantes pour les entrées (s, g), (*, g) et (*, \*) spécifiées.</span><span class="sxs-lookup"><span data-stu-id="20c52-118">Add to and delete from the outgoing interface list for the specified (s, g), (*, g), and (*, \*) entries.</span></span> <span data-ttu-id="20c52-119">Cette liste représente l’ensemble des interfaces sur lesquelles les données de ce groupe sont transférées.</span><span class="sxs-lookup"><span data-stu-id="20c52-119">This list represents the set of interfaces on which data for this group is forwarded.</span></span> <span data-ttu-id="20c52-120">Les données de ce groupe proviennent de la source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="20c52-120">The data for this group is from the specified source.</span></span></td>

</tr>
<tr class="even">

<td><span data-ttu-id="20c52-121">Envoyer des alertes aux protocoles de routage sous forme de rappels.</span><span class="sxs-lookup"><span data-stu-id="20c52-121">Send alerts to routing protocols in the form of callbacks.</span></span> <span data-ttu-id="20c52-122">Les événements suivants déclenchent le gestionnaire de groupe de multidiffusion pour appeler un rappel :</span><span class="sxs-lookup"><span data-stu-id="20c52-122">The following events trigger the multicast group manager to invoke a callback:</span></span>
<ul>
<li><span data-ttu-id="20c52-123">Joindre ou conserver des groupes ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="20c52-123">Join or leave groups ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="20c52-124">L’appartenance au groupe a changé par IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="20c52-124">Group membership changed by IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="20c52-125">Données reçues sur une interface incorrecte ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="20c52-125">Data received on wrong interface ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</span></span></li>
<li><span data-ttu-id="20c52-126">Données reçues à partir de nouvelles sources ou à un nouveau groupe ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> et <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="20c52-126">Data received from new sources or to a new group ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> and <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</span></span></li>
</ul></td>
<td><span data-ttu-id="20c52-127">À l’aide de ces rappels, le gestionnaire de groupe de multidiffusion est en mesure de coordonner le transfert de paquets lorsque plusieurs protocoles de routage de multidiffusion sont présents sur un routeur.</span><span class="sxs-lookup"><span data-stu-id="20c52-127">Using these callbacks, the multicast group manager is able to coordinate packet forwarding when several multicast routing protocols are present on a router.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="20c52-128">Énumérer les entrées de transfert de multidiffusion (MFEs) à l’aide des fonctions <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>et <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20c52-128">Enumerate the multicast forwarding entries (MFEs), using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>, and <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> functions.</span></span> <span data-ttu-id="20c52-129">Prendre des décisions sur les données multidiffusion en fonction des résultats de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="20c52-129">Make decisions about multicast data based on the results of the enumeration.</span></span></td>
<td><span data-ttu-id="20c52-130">Retourne le MFEs demandé.</span><span class="sxs-lookup"><span data-stu-id="20c52-130">Return the requested MFEs.</span></span> <span data-ttu-id="20c52-131">Retourne ERROR_NO_MORE éléments lorsqu’il n’y a plus de MFEs à retourner.</span><span class="sxs-lookup"><span data-stu-id="20c52-131">Return ERROR_NO_MORE ITEMS when there are no more MFEs to return.</span></span><br/></td>
<td><span data-ttu-id="20c52-132">Utilisez les fonctions <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> pour énumérer les statistiques MFE.</span><span class="sxs-lookup"><span data-stu-id="20c52-132">Use the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> functions to enumerate MFE statistics.</span></span> <span data-ttu-id="20c52-133">Pour obtenir un exemple complet de l’utilisation de ces fonctions, consultez <a href="administrative-application-scenario.md">scénario d’application administrative</a> .</span><span class="sxs-lookup"><span data-stu-id="20c52-133">See <a href="administrative-application-scenario.md">Administrative Application Scenario</a> for a complete example of using these functions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="20c52-134">Modifiez le voisin en amont dans un MFE à l’aide de la fonction <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20c52-134">Modify the upstream neighbor in an MFE using the <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> function.</span></span></td>

<td><span data-ttu-id="20c52-135">Les clients utilisent cette fonction pour modifier les informations relatives à l’interface entrante.</span><span class="sxs-lookup"><span data-stu-id="20c52-135">Clients use this function to modify the information regarding the incoming interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

