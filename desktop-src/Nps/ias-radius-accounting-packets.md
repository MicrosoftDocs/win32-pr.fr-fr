---
title: Journalisation avec le serveur NPS
description: Journalisation avec le serveur NPS
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315839"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="7a3bf-103">Journalisation avec le serveur NPS</span><span class="sxs-lookup"><span data-stu-id="7a3bf-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="7a3bf-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="7a3bf-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="7a3bf-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="7a3bf-107">Le tableau suivant décrit uniquement les aspects les plus importants des paquets de gestion de comptes RADIUS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="7a3bf-108">Le document demande de commentaires de gestion des comptes RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fournit des informations détaillées sur ces paquets.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="7a3bf-109">Les paquets de gestion des comptes RADIUS peuvent être répartis dans les catégories suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="7a3bf-110">Paquet de comptabilité</span><span class="sxs-lookup"><span data-stu-id="7a3bf-110">Accounting packet</span></span>  | <span data-ttu-id="7a3bf-111">Description</span><span class="sxs-lookup"><span data-stu-id="7a3bf-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3bf-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="7a3bf-112">Accounting-On</span></span>      | <span data-ttu-id="7a3bf-113">Envoyé par le serveur d’accès réseau (NAS) pour indiquer qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="7a3bf-114">Contient NAS-identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="7a3bf-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="7a3bf-115">Accounting-Off</span></span>     | <span data-ttu-id="7a3bf-116">Envoyé par le NAS pour indiquer qu’il est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="7a3bf-117">Contient NAS-identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="7a3bf-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="7a3bf-118">Accounting-Start</span></span>   | <span data-ttu-id="7a3bf-119">Envoyé par le NAS, après que l’utilisateur a été authentifié et autorisé, pour indiquer le début d’une session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="7a3bf-120">Contient UserID, NAS-identifier/IPAddress, ainsi que d’autres informations reçues du NAS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="7a3bf-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="7a3bf-121">Accounting-Stop</span></span>    | <span data-ttu-id="7a3bf-122">Envoyé par le NAS pour indiquer la fin d’une session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="7a3bf-123">Contient UserID, NAS-identifier/IPAddress, ainsi que d’autres informations reçues du NAS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="7a3bf-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="7a3bf-124">Accounting-Interim</span></span> | <span data-ttu-id="7a3bf-125">Peut être envoyé régulièrement par le NAS pour chaque utilisateur qui est connecté au NAS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="7a3bf-126">Cette fonctionnalité est généralement prise en charge dans les versions plus récentes de NAS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="7a3bf-127">Les problèmes suivants sont importants à prendre en compte lors de la collecte des informations de comptabilité mises à disposition via RADIUS :</span><span class="sxs-lookup"><span data-stu-id="7a3bf-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="7a3bf-128">Dans de rares cas, les paquets peuvent être perdus pendant la transmission et peuvent ne jamais atteindre le serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="7a3bf-129">Le serveur RADIUS n’est pas notifié si le NAS est abandonné.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="7a3bf-130">RNIS prend en charge plusieurs sessions et chaque session génère une paire de paquets de début/fin de compte.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="7a3bf-131">Il existe un attribut comptabilité appelé identificateur de session multiple qui identifie clairement de tels paquets de plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="7a3bf-132">Vérifiez l’identificateur de session multiple en plus de l’identificateur de session pour calculer le nombre de sessions.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="7a3bf-133">Demandes journalisées par NPS</span><span class="sxs-lookup"><span data-stu-id="7a3bf-133">Requests Logged by NPS</span></span>

<span data-ttu-id="7a3bf-134">Par défaut, NPS n’enregistre aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="7a3bf-135">Le serveur NPS peut être configuré à l’aide de l’interface utilisateur NPS (NPS. msc) pour enregistrer les requêtes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="7a3bf-136">Paquet journalisé</span><span class="sxs-lookup"><span data-stu-id="7a3bf-136">Logged packet</span></span>          | <span data-ttu-id="7a3bf-137">Description</span><span class="sxs-lookup"><span data-stu-id="7a3bf-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a3bf-138">Demande de comptabilité</span><span class="sxs-lookup"><span data-stu-id="7a3bf-138">Accounting Request</span></span>     | <span data-ttu-id="7a3bf-139">N’importe quel paquet comptable décrit dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="7a3bf-140">Demande d’authentification</span><span class="sxs-lookup"><span data-stu-id="7a3bf-140">Authentication Request</span></span> | <span data-ttu-id="7a3bf-141">Envoyé par le NAS pour le compte de l’utilisateur qui se connecte.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="7a3bf-142">Les entrées de journal contiennent uniquement des attributs entrants.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="7a3bf-143">Acceptation de l’authentification</span><span class="sxs-lookup"><span data-stu-id="7a3bf-143">Authentication Accept</span></span>  | <span data-ttu-id="7a3bf-144">Envoyé par le serveur NPS pour indiquer que la connexion utilisateur doit être acceptée.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="7a3bf-145">Les entrées de journal contiennent uniquement des attributs sortants.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="7a3bf-146">Rejet de l’authentification</span><span class="sxs-lookup"><span data-stu-id="7a3bf-146">Authentication Reject</span></span>  | <span data-ttu-id="7a3bf-147">Envoyé par le serveur NPS pour indiquer que la connexion utilisateur doit être rejetée.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="7a3bf-148">Les entrées de journal contiennent uniquement des attributs sortants.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="7a3bf-149">Les données consignées par NPS peuvent accéder à un fichier texte sur le serveur NPS ou à une base de données SQL centrale.</span><span class="sxs-lookup"><span data-stu-id="7a3bf-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="7a3bf-150">Pour plus d’informations sur la journalisation SQL NPS, consultez [programmabilité SQL](sql-programmability.md).</span><span class="sxs-lookup"><span data-stu-id="7a3bf-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a3bf-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a3bf-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a3bf-152">Service d’authentification Internet et serveur NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="7a3bf-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="7a3bf-153">Authentification, autorisation et gestion des comptes RADIUS</span><span class="sxs-lookup"><span data-stu-id="7a3bf-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="7a3bf-154">Utilisation d’un serveur d’État</span><span class="sxs-lookup"><span data-stu-id="7a3bf-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

