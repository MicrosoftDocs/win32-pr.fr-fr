---
description: Les fonctions de session de gestion de réseau contrôlent les sessions réseau établies entre les stations de travail et les serveurs. Les fonctions requièrent que le service serveur soit démarré sur le serveur.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Fonctions de session (gestion du partage réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c672abd7c976cb9f83fa4f387dd40d175879dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519863"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="b779b-104">Fonctions de session (gestion du partage réseau)</span><span class="sxs-lookup"><span data-stu-id="b779b-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="b779b-105">Les fonctions de session de gestion de réseau contrôlent les sessions réseau établies entre les stations de travail et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="b779b-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="b779b-106">Les fonctions requièrent que le service serveur soit démarré sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b779b-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="b779b-107">Les fonctions de session sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b779b-107">The session functions are listed following.</span></span>



| <span data-ttu-id="b779b-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="b779b-108">Function</span></span>                                       | <span data-ttu-id="b779b-109">Description</span><span class="sxs-lookup"><span data-stu-id="b779b-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b779b-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="b779b-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="b779b-111">Supprime les connexions en cours entre une station de travail et un serveur. met fin à la session réseau.</span><span class="sxs-lookup"><span data-stu-id="b779b-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="b779b-112">**NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="b779b-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="b779b-113">Retourne des informations sur toutes les sessions en cours établies pour un serveur.</span><span class="sxs-lookup"><span data-stu-id="b779b-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="b779b-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="b779b-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="b779b-115">Retourne des informations sur une session particulière.</span><span class="sxs-lookup"><span data-stu-id="b779b-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="b779b-116">Une *session* est un lien entre une station de travail et un serveur.</span><span class="sxs-lookup"><span data-stu-id="b779b-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="b779b-117">Une session est établie la première fois qu’une station de travail établit une connexion à une ressource partagée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b779b-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="b779b-118">Jusqu’à la fin de la session, toutes les connexions supplémentaires entre la station de travail et le serveur font partie de la même session.</span><span class="sxs-lookup"><span data-stu-id="b779b-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="b779b-119">Pour mettre fin à une session, une application sur l’extrémité serveur d’une connexion appelle la fonction [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .</span><span class="sxs-lookup"><span data-stu-id="b779b-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="b779b-120">Les fonctions de session de gestion de réseau gèrent les informations par utilisateur avec le paramètre *username* .</span><span class="sxs-lookup"><span data-stu-id="b779b-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="b779b-121">Étant donné qu’il peut y avoir plusieurs utilisateurs par session, ce paramètre est nécessaire pour accéder aux informations spécifiques à l’utilisateur pour la session.</span><span class="sxs-lookup"><span data-stu-id="b779b-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="b779b-122">Les fonctions de session sont disponibles à cinq niveaux d’informations :</span><span class="sxs-lookup"><span data-stu-id="b779b-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="b779b-123">**Informations de SESSION \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="b779b-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="b779b-124">**Informations de SESSION \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b779b-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="b779b-125">**\_Informations sur la session \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b779b-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="b779b-126">**Informations de SESSION \_ \_ 10**</span><span class="sxs-lookup"><span data-stu-id="b779b-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="b779b-127">**Informations de SESSION \_ \_ 502**</span><span class="sxs-lookup"><span data-stu-id="b779b-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="b779b-128">Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de session de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="b779b-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="b779b-129">Pour plus d’informations, consultez [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) et [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span><span class="sxs-lookup"><span data-stu-id="b779b-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
