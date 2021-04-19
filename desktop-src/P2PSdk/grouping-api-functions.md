---
description: 'L’API de regroupement utilise les fonctions suivantes :'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Fonctions d’API de regroupement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517086"
---
# <a name="grouping-api-functions"></a><span data-ttu-id="929ac-103">Fonctions d’API de regroupement</span><span class="sxs-lookup"><span data-stu-id="929ac-103">Grouping API Functions</span></span>

<span data-ttu-id="929ac-104">L’API de regroupement utilise les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="929ac-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="929ac-105">Fonctions d’initialisation et de nettoyage des groupes</span><span class="sxs-lookup"><span data-stu-id="929ac-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="929ac-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-106">Function</span></span>                                       | <span data-ttu-id="929ac-107">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-108">**PeerGroupShutdown**</span><span class="sxs-lookup"><span data-stu-id="929ac-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="929ac-109">Ferme un groupe homologue créé avec [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) et supprime toutes les ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="929ac-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="929ac-110">**PeerGroupStartup**</span><span class="sxs-lookup"><span data-stu-id="929ac-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="929ac-111">Initie un groupe homologue à l’aide d’une version demandée de l’infrastructure homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="929ac-112">Fonctions de création de groupe et d’accès</span><span class="sxs-lookup"><span data-stu-id="929ac-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="929ac-113">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-113">Function</span></span>                                                                       | <span data-ttu-id="929ac-114">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-115">**PeerGroupClose**</span><span class="sxs-lookup"><span data-stu-id="929ac-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="929ac-116">Invalide le descripteur du groupe homologue obtenu par un appel précédent à la fonction [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .</span><span class="sxs-lookup"><span data-stu-id="929ac-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="929ac-117">**PeerGroupConnect**</span><span class="sxs-lookup"><span data-stu-id="929ac-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="929ac-118">Lance une recherche PNRP pour un groupe homologue et tente de s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="929ac-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="929ac-119">Une fois que cette fonction a été appelée avec succès, un homologue peut communiquer avec les autres membres du groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="929ac-120">**PeerGroupConnectByAddress**</span><span class="sxs-lookup"><span data-stu-id="929ac-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="929ac-121">Tente de se connecter au groupe homologue auquel les autres pairs avec des adresses IPv6 connues participent.</span><span class="sxs-lookup"><span data-stu-id="929ac-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="929ac-122">**PeerGroupCreate**</span><span class="sxs-lookup"><span data-stu-id="929ac-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="929ac-123">Crée un nouveau groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="929ac-124">**PeerGroupCreateInvitation**</span><span class="sxs-lookup"><span data-stu-id="929ac-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="929ac-125">Retourne une chaîne XML qui peut être utilisée par l’homologue spécifié pour joindre un groupe.</span><span class="sxs-lookup"><span data-stu-id="929ac-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="929ac-126">**PeerGroupCreatePasswordInvitation**</span><span class="sxs-lookup"><span data-stu-id="929ac-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="929ac-127">Retourne une chaîne XML qui peut être utilisée par l’homologue spécifié pour joindre un groupe avec un mot de passe correspondant.</span><span class="sxs-lookup"><span data-stu-id="929ac-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="929ac-128">**PeerGroupDelete**</span><span class="sxs-lookup"><span data-stu-id="929ac-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="929ac-129">Supprime les données locales et le certificat associé à un groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="929ac-130">**PeerGroupGetStatus**</span><span class="sxs-lookup"><span data-stu-id="929ac-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="929ac-131">Récupère l’état actuel d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="929ac-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="929ac-132">**PeerGroupIssueCredentials**</span><span class="sxs-lookup"><span data-stu-id="929ac-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="929ac-133">Émet des informations d’identification, y compris un GMC, vers une identité spécifique et retourne éventuellement une chaîne XML d’invitation que l’homologue invité peut utiliser pour joindre un groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="929ac-134">**PeerGroupJoin**</span><span class="sxs-lookup"><span data-stu-id="929ac-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="929ac-135">Permet à un homologue avec une invitation de joindre un groupe homologue existant.</span><span class="sxs-lookup"><span data-stu-id="929ac-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="929ac-136">**PeerGroupOpen**</span><span class="sxs-lookup"><span data-stu-id="929ac-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="929ac-137">Ouvre un groupe homologue qu’un homologue a créé ou joint.</span><span class="sxs-lookup"><span data-stu-id="929ac-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="929ac-138">**PeerGroupParseInvitation**</span><span class="sxs-lookup"><span data-stu-id="929ac-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="929ac-139">Retourne une structure d' [**\_ \_ informations d’invitation de pairs**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) avec les détails d’une invitation spécifique.</span><span class="sxs-lookup"><span data-stu-id="929ac-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="929ac-140">**PeerGroupPasswordJoin**</span><span class="sxs-lookup"><span data-stu-id="929ac-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="929ac-141">Permet à un homologue disposant d’une invitation et du mot de passe correct de rejoindre un groupe homologue protégé par mot de passe.</span><span class="sxs-lookup"><span data-stu-id="929ac-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="929ac-142">Fonctions d’informations de groupe et de membre</span><span class="sxs-lookup"><span data-stu-id="929ac-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="929ac-143">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-143">Function</span></span>                                                 | <span data-ttu-id="929ac-144">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-145">**PeerGroupEnumMembers**</span><span class="sxs-lookup"><span data-stu-id="929ac-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="929ac-146">Crée une énumération des membres du groupe homologue disponibles et des informations d’appartenance associées.</span><span class="sxs-lookup"><span data-stu-id="929ac-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="929ac-147">**PeerGroupGetProperties**</span><span class="sxs-lookup"><span data-stu-id="929ac-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="929ac-148">Récupère des informations sur les propriétés d’un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="929ac-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="929ac-149">**PeerGroupSetProperties**</span><span class="sxs-lookup"><span data-stu-id="929ac-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="929ac-150">Définit les propriétés actuelles du groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-150">Sets the current peer group properties.</span></span> <span data-ttu-id="929ac-151">Dans la version 1,0 de cette API, seul le créateur du groupe homologue peut effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="929ac-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="929ac-152">Fonctions de gestion des enregistrements et des enregistrements</span><span class="sxs-lookup"><span data-stu-id="929ac-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="929ac-153">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-153">Function</span></span>                                                 | <span data-ttu-id="929ac-154">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-155">**PeerGroupAddRecord**</span><span class="sxs-lookup"><span data-stu-id="929ac-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="929ac-156">Ajoute un nouvel enregistrement au groupe homologue, qui est propagé à tous les homologues participants.</span><span class="sxs-lookup"><span data-stu-id="929ac-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="929ac-157">**PeerGroupDeleteRecord**</span><span class="sxs-lookup"><span data-stu-id="929ac-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="929ac-158">Supprime un enregistrement d’un groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="929ac-159">Seul le créateur d’un enregistrement peut le supprimer.</span><span class="sxs-lookup"><span data-stu-id="929ac-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="929ac-160">**PeerGroupEnumRecords**</span><span class="sxs-lookup"><span data-stu-id="929ac-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="929ac-161">Crée une énumération des enregistrements du groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="929ac-162">**PeerGroupGetRecord**</span><span class="sxs-lookup"><span data-stu-id="929ac-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="929ac-163">Récupère un enregistrement de groupe spécifique.</span><span class="sxs-lookup"><span data-stu-id="929ac-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="929ac-164">**PeerGroupSearchRecords**</span><span class="sxs-lookup"><span data-stu-id="929ac-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="929ac-165">Recherche dans la base de données du groupe homologue local les enregistrements qui correspondent aux critères fournis.</span><span class="sxs-lookup"><span data-stu-id="929ac-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="929ac-166">**PeerGroupUpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="929ac-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="929ac-167">Met à jour un enregistrement dans un groupe homologue spécifique.</span><span class="sxs-lookup"><span data-stu-id="929ac-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="929ac-168">Fonctions d’importation/exportation de base de données de groupe</span><span class="sxs-lookup"><span data-stu-id="929ac-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="929ac-169">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-169">Function</span></span>                                                   | <span data-ttu-id="929ac-170">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-171">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="929ac-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="929ac-172">Exporte une base de données de groupe homologue dans un fichier spécifique, qui peut être transporté vers un autre ordinateur et importé avec la fonction [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) .</span><span class="sxs-lookup"><span data-stu-id="929ac-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="929ac-173">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="929ac-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="929ac-174">Importe une base de données de groupe homologue à partir d’un fichier local.</span><span class="sxs-lookup"><span data-stu-id="929ac-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="929ac-175">Fonctions de connexion directe</span><span class="sxs-lookup"><span data-stu-id="929ac-175">Direct Connection Functions</span></span>



| <span data-ttu-id="929ac-176">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-176">Function</span></span>                                                                 | <span data-ttu-id="929ac-177">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="929ac-178">**PeerGroupCloseDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="929ac-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="929ac-179">Ferme une connexion directe spécifique entre deux homologues.</span><span class="sxs-lookup"><span data-stu-id="929ac-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="929ac-180">**PeerGroupEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="929ac-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="929ac-181">Crée une énumération des connexions actuellement actives sur l’homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="929ac-182">**PeerGroupOpenDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="929ac-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="929ac-183">Établit une connexion directe avec un autre homologue dans un groupe homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="929ac-184">**PeerGroupSendData**</span><span class="sxs-lookup"><span data-stu-id="929ac-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="929ac-185">Envoie des données à un membre via un voisin ou une connexion directe.</span><span class="sxs-lookup"><span data-stu-id="929ac-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="929ac-186">Infrastructure des événements de groupe</span><span class="sxs-lookup"><span data-stu-id="929ac-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="929ac-187">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-187">Function</span></span>                                                     | <span data-ttu-id="929ac-188">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-189">**PeerGroupGetEventData**</span><span class="sxs-lookup"><span data-stu-id="929ac-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="929ac-190">Permet à une application de récupérer les données retournées par un événement de regroupement.</span><span class="sxs-lookup"><span data-stu-id="929ac-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="929ac-191">**PeerGroupRegisterEvent**</span><span class="sxs-lookup"><span data-stu-id="929ac-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="929ac-192">Inscrit un homologue pour des événements de groupe homologue spécifiques.</span><span class="sxs-lookup"><span data-stu-id="929ac-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="929ac-193">**PeerGroupUnregisterEvent**</span><span class="sxs-lookup"><span data-stu-id="929ac-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="929ac-194">Annule l’inscription d’un homologue de la notification d’événements homologues associée au handle d’événement fourni.</span><span class="sxs-lookup"><span data-stu-id="929ac-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="929ac-195">Fonctions de conversion de temps de groupe</span><span class="sxs-lookup"><span data-stu-id="929ac-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="929ac-196">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-196">Function</span></span>                                                                     | <span data-ttu-id="929ac-197">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-198">**PeerGroupPeerTimeToUniversalTime**</span><span class="sxs-lookup"><span data-stu-id="929ac-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="929ac-199">Convertit la valeur de temps de référence gérée du groupe homologue en une valeur de temps localisée appropriée pour l’affichage sur un ordinateur homologue.</span><span class="sxs-lookup"><span data-stu-id="929ac-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="929ac-200">**PeerGroupUniversalTimeToPeerTime**</span><span class="sxs-lookup"><span data-stu-id="929ac-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="929ac-201">Convertit une valeur d’heure locale de l’ordinateur d’un homologue en une valeur de temps de groupe pair commune.</span><span class="sxs-lookup"><span data-stu-id="929ac-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="929ac-202">Fonctions de configuration de groupe</span><span class="sxs-lookup"><span data-stu-id="929ac-202">Group Configuration Functions</span></span>



| <span data-ttu-id="929ac-203">Fonction</span><span class="sxs-lookup"><span data-stu-id="929ac-203">Function</span></span>                                               | <span data-ttu-id="929ac-204">Description</span><span class="sxs-lookup"><span data-stu-id="929ac-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="929ac-205">**PeerGroupExportConfig**</span><span class="sxs-lookup"><span data-stu-id="929ac-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="929ac-206">Exporte la configuration de groupe pour un homologue sous la forme d’une chaîne XML qui contient l’identité, le nom du groupe et le GMC pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="929ac-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="929ac-207">**PeerGroupImportConfig**</span><span class="sxs-lookup"><span data-stu-id="929ac-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="929ac-208">Importe une configuration de groupe homologue pour une identité basée sur les paramètres spécifiques d’une chaîne de configuration XML fournie.</span><span class="sxs-lookup"><span data-stu-id="929ac-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



