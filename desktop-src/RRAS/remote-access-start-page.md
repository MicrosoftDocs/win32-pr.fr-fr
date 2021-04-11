---
title: Accès à distance
description: Utilisez le service d’accès à distance (RAS) pour créer des applications clientes.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS du service d’accès à distance
- RAS RAS
- RAS du service d’accès à distance, page de démarrage
- RAS RAS, voir accès à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101297"
---
# <a name="remote-access"></a><span data-ttu-id="298e3-107">Accès à distance</span><span class="sxs-lookup"><span data-stu-id="298e3-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="298e3-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="298e3-108">Purpose</span></span>

<span data-ttu-id="298e3-109">Utilisez le service d’accès à distance (RAS) pour créer des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="298e3-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="298e3-110">Ces applications affichent les boîtes de dialogue courantes RAS, gèrent les connexions et les appareils d’accès à distance et manipulent les entrées d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="298e3-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="298e3-111">RAS fournit également la nouvelle génération de fonctionnalités serveur pour le service d’accès à distance (RAS) pour Windows.</span><span class="sxs-lookup"><span data-stu-id="298e3-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="298e3-112">La fonctionnalité de serveur RRAS suit et s’appuie sur le service d’accès à distance (RAS).</span><span class="sxs-lookup"><span data-stu-id="298e3-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="298e3-113">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="298e3-113">Where applicable</span></span>

<span data-ttu-id="298e3-114">Le service d’accès à distance est applicable dans n’importe quel environnement informatique qui utilise une liaison de réseau étendu (WAN) ou un réseau privé virtuel (VPN).</span><span class="sxs-lookup"><span data-stu-id="298e3-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="298e3-115">RAS permet de connecter un ordinateur client distant à un serveur réseau via une liaison de réseau étendu (WAN) ou un réseau privé virtuel (VPN).</span><span class="sxs-lookup"><span data-stu-id="298e3-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="298e3-116">L’ordinateur distant fonctionne alors sur le réseau local du serveur comme si l’ordinateur distant était directement connecté au réseau local.</span><span class="sxs-lookup"><span data-stu-id="298e3-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="298e3-117">L’API RAS permet aux programmeurs d’accéder par programme aux fonctionnalités de RAS.</span><span class="sxs-lookup"><span data-stu-id="298e3-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="298e3-118">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="298e3-118">Developer audience</span></span>

<span data-ttu-id="298e3-119">L’API RAS est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="298e3-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="298e3-120">Les programmeurs Microsoft Visual Basic peuvent également trouver l’API utile.</span><span class="sxs-lookup"><span data-stu-id="298e3-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="298e3-121">Les programmeurs doivent être familiarisés avec les concepts de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="298e3-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="298e3-122">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="298e3-122">Run-time requirements</span></span>

<span data-ttu-id="298e3-123">Certaines fonctions de l’API RAS sont uniquement prises en charge sur les serveurs réseau et les autres fonctions sont prises en charge uniquement sur les clients réseau.</span><span class="sxs-lookup"><span data-stu-id="298e3-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="298e3-124">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="298e3-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="298e3-125">La [fonctionnalité RAS améliorée](function-comparison-windows-2000-versus-rras-redistributable.md) de RRAS est disponible pour Windows NT Server 4,0 en installant le [package redistribuable RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span><span class="sxs-lookup"><span data-stu-id="298e3-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="298e3-126">Toutes les fonctionnalités du service RRAS sont intégrées à Windows 2000 Server, Windows Server 2003 et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="298e3-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="298e3-127">Les applications RRAS ne peuvent pas s’exécuter sur Windows NT Workstation 4,0 ou sur des systèmes d’exploitation clients, tels que Windows 95.</span><span class="sxs-lookup"><span data-stu-id="298e3-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="298e3-128">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="298e3-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="298e3-129">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="298e3-129">In this section</span></span>



| <span data-ttu-id="298e3-130">Rubrique</span><span class="sxs-lookup"><span data-stu-id="298e3-130">Topic</span></span>                                                                                             | <span data-ttu-id="298e3-131">Description</span><span class="sxs-lookup"><span data-stu-id="298e3-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="298e3-132">Service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="298e3-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="298e3-133">Le service d’accès à distance (RAS) fournit des fonctionnalités d’accès à distance aux applications clientes sur des ordinateurs exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="298e3-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="298e3-134">Administration du service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="298e3-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="298e3-135">L’administration du service d’accès à distance fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS.</span><span class="sxs-lookup"><span data-stu-id="298e3-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="298e3-136">À l’aide de ces fonctions, vous pouvez développer une application d’administration de serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="298e3-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="298e3-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="298e3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="298e3-138">Routage</span><span class="sxs-lookup"><span data-stu-id="298e3-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="298e3-139">Protocoles de routage</span><span class="sxs-lookup"><span data-stu-id="298e3-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 





