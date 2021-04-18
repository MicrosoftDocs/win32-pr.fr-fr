---
title: Utilisation d’ADSI avec Exchange
description: Pour Exchange 2000, les informations relatives à l’utilisation d’ADSI avec Exchange sont contenues dans le kit de développement logiciel (SDK) Exchange 2000. Pour plus d’informations, consultez tâches de gestion pour ADSI.
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI pour Exchange ADSI
- ADSI pour Exchange ADSI, boîtes aux lettres
- ADSI pour Exchange ADSI, boîtes aux lettres, création
- ADSI pour Exchange ADSI, boîtes aux lettres, suppression
- ADSI pour Exchange ADSI, boîtes aux lettres, définition du descripteur de sécurité sur
- ADSI pour Exchange ADSI, boîtes aux lettres, recherche d’un serveur local pour
- ADSI pour Exchange ADSI, obtention et modification de messages
- ADSI pour Exchange ADSI, descripteurs de sécurité
- ADSI pour Exchange ADSI, descripteurs de sécurité, manipulation
- ADSI pour Exchange ADSI, descripteurs de sécurité, définition
- ADSI pour Exchange ADSI, conteneur de destinataires
- ADSI pour Exchange ADSI, affichage des propriétés de l’objet Exchange
- ADSI pour Exchange ADSI, conteneur de destinataires, personnalisé
- ADSI pour Exchange ADSI, Exchange Server
- ADSI pour Exchange ADSI, Exchange Server, affichage et modification de schéma
- ADSI pour Exchange ADSI, Exchange Server, listing Server version
- ADSI pour Exchange ADSI, Exchange Server, organisation et nom de site
- ADSI pour Exchange ADSI, Exchange Server, recherche d’un serveur d’hébergement de boîte aux lettres
- ADSI pour Exchange ADSI, adresses de messagerie, récupération
- ADSI pour Exchange ADSI, listes de distribution, création
- ADSI pour Exchange ADSI, entrées masquées ou supprimées
- ADSI pour Exchange ADSI, récupération des modifications du service d’annuaire
- ADSI pour Exchange ADSI, taille du message
- ADSI pour Exchange ADSI, résolution des problèmes
- boîte aux lettres ADSI
- boîtes aux lettres ADSI, création
- boîtes aux lettres ADSI, suppression
- boîtes aux lettres ADSI, définition du descripteur de sécurité sur
- boîtes aux lettres ADSI, Rechercher le serveur d’hébergement pour
- messages ADSI, obtention et modification
- Exchange ADSI
- Exchange ADSI, boîtes aux lettres
- Exchange ADSI, boîtes aux lettres, création
- Exchange ADSI, boîtes aux lettres, suppression
- Exchange ADSI, boîtes aux lettres, définition du descripteur de sécurité sur
- Exchange ADSI, boîtes aux lettres, recherche d’un serveur local pour
- Exchange ADSI, obtention et modification de messages
- Exchange ADSI, descripteurs de sécurité
- Exchange ADSI, descripteurs de sécurité, manipulation
- Exchange ADSI, descripteurs de sécurité, définition
- Exchange ADSI, conteneur Destinataires
- Exchange ADSI, affichage des propriétés d’un objet Exchange
- Exchange ADSI, conteneur destinataires, personnalisé
- Exchange ADSI, Exchange Server
- Exchange ADSI, Exchange Server, affichage et modification de schéma
- Exchange ADSI, Exchange Server, listing Server version
- Exchange ADSI, Exchange Server, organisation et nom de site
- Exchange ADSI, Exchange Server, recherche d’un serveur d’hébergement de boîte aux lettres
- Exchange ADSI, adresses de messagerie, récupération
- Exchange ADSI, listes de distribution, création
- Exchange ADSI, entrées masquées ou supprimées
- Exchange ADSI, récupération des modifications du service d’annuaire
- Exchange ADSI, taille des messages
- Exchange ADSI, résolution des problèmes
- descripteurs de sécurité ADSI, pour les objets Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106512126"
---
# <a name="using-adsi-with-exchange"></a><span data-ttu-id="05c43-159">Utilisation d’ADSI avec Exchange</span><span class="sxs-lookup"><span data-stu-id="05c43-159">Using ADSI with Exchange</span></span>

<span data-ttu-id="05c43-160">Pour Exchange 2000, les informations relatives à l’utilisation d’ADSI avec Exchange sont contenues dans le kit de développement logiciel (SDK) Exchange 2000.</span><span class="sxs-lookup"><span data-stu-id="05c43-160">For Exchange 2000, information for using ADSI with Exchange is contained in the Exchange 2000 SDK.</span></span> <span data-ttu-id="05c43-161">Pour plus d’informations, consultez [tâches de gestion pour ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="05c43-161">For more information, see [Management Tasks for ADSI](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65)).</span></span>

<span data-ttu-id="05c43-162">Les tâches suivantes se trouvent dans cette section :</span><span class="sxs-lookup"><span data-stu-id="05c43-162">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="05c43-163">Création d’une URL d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="05c43-163">Creating a user URL</span></span>
-   <span data-ttu-id="05c43-164">Création de chemins d’accès Active Directory</span><span class="sxs-lookup"><span data-stu-id="05c43-164">Building Active Directory paths</span></span>
-   <span data-ttu-id="05c43-165">Énumération des serveurs Exchange 2000 avec ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-165">Enumerating Exchange 2000 servers with ADSI</span></span>
-   <span data-ttu-id="05c43-166">Manipulation des attributs d’extension avec ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-166">Manipulating extension attributes with ADSI</span></span>
-   <span data-ttu-id="05c43-167">Ajout/suppression d’un objet Manager avec ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-167">Adding/removing a manager object with ADSI</span></span>
-   <span data-ttu-id="05c43-168">Énumération des propriétés d’objet Exchange avec ADSI/ADO</span><span class="sxs-lookup"><span data-stu-id="05c43-168">Enumerating Exchange object properties with ADSI/ADO</span></span>
-   <span data-ttu-id="05c43-169">Récupération d’un nom unique Exchange hérité avec ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-169">Retrieving a legacy Exchange distinguished name with ADSI</span></span>
-   <span data-ttu-id="05c43-170">Recherche du nom de l’organisation Exchange à l’aide d’ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-170">Finding the Exchange organization name using ADSI</span></span>
-   <span data-ttu-id="05c43-171">Recherche de listes d’adresses Exchange avec ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-171">Finding Exchange address lists with ADSI</span></span>
-   <span data-ttu-id="05c43-172">Création d’une liste de distribution à l’aide de CDOEXM et ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-172">Creating a distribution list using CDOEXM and ADSI</span></span>
-   <span data-ttu-id="05c43-173">Définition de la restriction des messages sur un serveur virtuel SMTP à l’aide d’ADSI</span><span class="sxs-lookup"><span data-stu-id="05c43-173">Setting message restriction on an SMTP virtual server using ADSI</span></span>

<span data-ttu-id="05c43-174">Pour Exchange 5,5, la référence ADSI et l’utilisation des informations sont disponibles dans le Guide d' [échange ADSI](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) .</span><span class="sxs-lookup"><span data-stu-id="05c43-174">For Exchange 5.5, the ADSI reference and using information can be found in the [ADSI Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) guide.</span></span>

<span data-ttu-id="05c43-175">Les tâches suivantes se trouvent dans cette section :</span><span class="sxs-lookup"><span data-stu-id="05c43-175">The following tasks can be found in this section:</span></span>

-   <span data-ttu-id="05c43-176">Affichage et modification du schéma Exchange Server</span><span class="sxs-lookup"><span data-stu-id="05c43-176">Viewing and modifying the Exchange Server Schema</span></span>
-   <span data-ttu-id="05c43-177">Affichage des propriétés brutes d’un objet Exchange</span><span class="sxs-lookup"><span data-stu-id="05c43-177">Viewing the raw properties of an Exchange object</span></span>
-   <span data-ttu-id="05c43-178">Création d’une boîte aux lettres Exchange</span><span class="sxs-lookup"><span data-stu-id="05c43-178">Creating an Exchange mailbox</span></span>
-   <span data-ttu-id="05c43-179">Définition du descripteur de sécurité sur une boîte aux lettres Exchange</span><span class="sxs-lookup"><span data-stu-id="05c43-179">Setting the security descriptor on an Exchange mailbox</span></span>
-   <span data-ttu-id="05c43-180">Manipulation des descripteurs de sécurité et des SID</span><span class="sxs-lookup"><span data-stu-id="05c43-180">Manipulating security descriptors and SIDs</span></span>
-   <span data-ttu-id="05c43-181">Suppression d’un objet de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="05c43-181">Deleting a mailbox object</span></span>
-   <span data-ttu-id="05c43-182">Création d’un destinataire personnalisé</span><span class="sxs-lookup"><span data-stu-id="05c43-182">Creating a custom recipient</span></span>
-   <span data-ttu-id="05c43-183">Création d’un conteneur Destinataires</span><span class="sxs-lookup"><span data-stu-id="05c43-183">Creating a recipients container</span></span>
-   <span data-ttu-id="05c43-184">Obtention du nom de l’organisation et du site à partir d’un serveur</span><span class="sxs-lookup"><span data-stu-id="05c43-184">Getting the organization and site name from a server</span></span>
-   <span data-ttu-id="05c43-185">Affichage de la version Exchange Server de tous les serveurs de l’Organisation</span><span class="sxs-lookup"><span data-stu-id="05c43-185">Listing the Exchange server version of all the servers in the organization</span></span>
-   <span data-ttu-id="05c43-186">Recherche du serveur d’hébergement d’une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="05c43-186">Finding the home server of a mailbox</span></span>
-   <span data-ttu-id="05c43-187">Récupération des adresses de messagerie</span><span class="sxs-lookup"><span data-stu-id="05c43-187">Retrieving email addresses</span></span>
-   <span data-ttu-id="05c43-188">Accès aux entrées masquées ou supprimées</span><span class="sxs-lookup"><span data-stu-id="05c43-188">Accessing hidden or deleted entries</span></span>
-   <span data-ttu-id="05c43-189">Récupération des modifications apportées au service d’annuaire</span><span class="sxs-lookup"><span data-stu-id="05c43-189">Retrieving changes made to the directory service</span></span>
-   <span data-ttu-id="05c43-190">Création d’une liste de distribution à partir des résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="05c43-190">Creating a distribution list from the results of a query</span></span>
-   <span data-ttu-id="05c43-191">Obtention ou modification de la taille des messages</span><span class="sxs-lookup"><span data-stu-id="05c43-191">Getting or modifying message size</span></span>
-   <span data-ttu-id="05c43-192">Utilisation des codes d’erreur LDAP pour résoudre les problèmes</span><span class="sxs-lookup"><span data-stu-id="05c43-192">Using LDAP error codes to troubleshoot problems</span></span>

 

 