---
title: Utilisation d’un serveur d’État
description: NPS effectue l’authentification à l’aide d’une base de données configurée sur le site du serveur NPS.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511081"
---
# <a name="working-with-a-state-server"></a><span data-ttu-id="e8706-103">Utilisation d’un serveur d’État</span><span class="sxs-lookup"><span data-stu-id="e8706-103">Working With a State Server</span></span>

> [!Note]  
> <span data-ttu-id="e8706-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e8706-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="e8706-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="e8706-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="e8706-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="e8706-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="e8706-107">NPS effectue l’authentification à l’aide d’une base de données configurée sur le site du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="e8706-107">NPS performs authentication using a database that is configured at the NPS server site.</span></span> <span data-ttu-id="e8706-108">Cette base de données d’authentification peut être la base de données utilisateur d’un domaine Windows, ou elle peut créer les informations utilisateur obtenues à partir du Active Directory Windows.</span><span class="sxs-lookup"><span data-stu-id="e8706-108">This authentication database could be the user database for a Windows Domain or it could draw upon the user information obtained from the Windows Active Directory.</span></span> <span data-ttu-id="e8706-109">Le diagramme suivant illustre une configuration classique qui montre comment NPS interagit avec les bases de données d’authentification, telles qu’une base de données utilisateur de domaine Windows ou Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8706-109">The following diagram illustrates a typical configuration that shows how NPS interacts with authentication databases such as a Windows Domain user database or Active Directory.</span></span> <span data-ttu-id="e8706-110">Le diagramme montre également comment NPS peut interagir avec un serveur d’état fourni par un tiers.</span><span class="sxs-lookup"><span data-stu-id="e8706-110">The diagram also shows how NPS could interact with a state server that is provided by a third party.</span></span> <span data-ttu-id="e8706-111">L’objectif principal d’un serveur d’État est de limiter le nombre de sessions d’ouverture de session simultanées qu’un seul utilisateur peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="e8706-111">The primary purpose of a state server is to limit the number of simultaneous logon sessions a single user can run.</span></span>

![NPS qui interagit avec le serveur d’État et les bases de données d’authentification](images/ias02.png)

<span data-ttu-id="e8706-113">Il existe deux points d’interaction entre NPS et le serveur d’État.</span><span class="sxs-lookup"><span data-stu-id="e8706-113">There are two points of interaction between NPS and the state server.</span></span> <span data-ttu-id="e8706-114">Une interaction a lieu lorsque NPS reçoit une demande d’authentification du NAS.</span><span class="sxs-lookup"><span data-stu-id="e8706-114">One interaction takes place when NPS receives an authentication request from the NAS.</span></span> <span data-ttu-id="e8706-115">Le serveur d’État fournit des informations à partir de sa base de données pour déterminer s’il faut accepter ou refuser la demande.</span><span class="sxs-lookup"><span data-stu-id="e8706-115">The state server provides information from its database to determine whether to accept or deny the request.</span></span> <span data-ttu-id="e8706-116">L’autre interaction a lieu lorsque NPS reçoit des demandes de gestion de compte du NAS.</span><span class="sxs-lookup"><span data-stu-id="e8706-116">The other interaction takes place when NPS receives accounting requests from the NAS.</span></span> <span data-ttu-id="e8706-117">Le serveur d’État utilise ces informations pour mettre à jour sa base de données.</span><span class="sxs-lookup"><span data-stu-id="e8706-117">The state server uses the information form these accounting requests to update its database.</span></span>

<span data-ttu-id="e8706-118">Pour plus d’informations sur les serveurs d’État, consultez :</span><span class="sxs-lookup"><span data-stu-id="e8706-118">For more information on state servers see:</span></span>

-   [<span data-ttu-id="e8706-119">Considérations relatives à la conception du serveur d’État</span><span class="sxs-lookup"><span data-stu-id="e8706-119">State Server Design Considerations</span></span>](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a><span data-ttu-id="e8706-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e8706-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8706-121">Service d’authentification Internet et serveur NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="e8706-121">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="e8706-122">Authentification, autorisation et gestion des comptes RADIUS</span><span class="sxs-lookup"><span data-stu-id="e8706-122">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="e8706-123">Journalisation avec le serveur NPS</span><span class="sxs-lookup"><span data-stu-id="e8706-123">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 