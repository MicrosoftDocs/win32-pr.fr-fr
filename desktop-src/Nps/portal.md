---
title: Serveur de stratégie réseau
description: Le serveur NPS (Network Policy Server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS (Remote Authentication Dial-in User Service).
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315443"
---
# <a name="network-policy-server"></a><span data-ttu-id="b7bc8-103">Serveur de stratégie réseau</span><span class="sxs-lookup"><span data-stu-id="b7bc8-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="b7bc8-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="b7bc8-104">Purpose</span></span>

<span data-ttu-id="b7bc8-105">Le serveur NPS (Network Policy Server) est l’implémentation Microsoft d’un serveur et d’un proxy RADIUS (Remote Authentication Dial-in User Service).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="b7bc8-106">Il s’agit du successeur du service d’authentification Internet (IAS).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="b7bc8-107">En tant que serveur RADIUS, NPS effectue l’authentification, l’autorisation et la gestion des comptes pour les connexions sans fil, de commutateur d’authentification et d’accès à distance et de réseau privé virtuel (VPN).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="b7bc8-108">NPS est également un serveur d’évaluateur d’intégrité pour la protection d’accès réseau (NAP).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="b7bc8-109">NPS effectue l’authentification et l’autorisation des tentatives de connexion réseau et, en fonction des stratégies de contrôle d’intégrité du système configurées, évalue la conformité de l’intégrité de l’ordinateur et détermine comment limiter l’accès réseau ou la communication d’un ordinateur non conforme.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="b7bc8-110">Il s’agit d’une nouvelle fonctionnalité spécifique à NPS uniquement. IAS ne la prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="b7bc8-111">Consultez [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) pour obtenir une liste complète des fonctionnalités nouvelles sur NPS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="b7bc8-112">NPS comprend deux ensembles d’API : l’API d’extensions NPS et l’API d’objets de données serveur (SDO).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="b7bc8-113">L’API des extensions NPS et l’API SDO sont également prises en charge par le précurseur du serveur NPS, le service d’authentification Internet.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="b7bc8-114">L’API extensions NPS peut être utilisée pour étendre les méthodes d’authentification, d’autorisation et de gestion des comptes offertes par NPS et précédemment par IAS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="b7bc8-115">L’API des objets de données du serveur peut être utilisée pour manipuler la configuration de la stratégie réseau sur un ordinateur exécutant NPS ou IAS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="b7bc8-116">Les stratégies réseau dans NPS sont équivalentes aux stratégies d’accès à distance dans IAS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="b7bc8-117">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="b7bc8-117">Developer audience</span></span>

<span data-ttu-id="b7bc8-118">L’API extensions NPS est conçue pour être utilisée par les programmeurs qui utilisent le logiciel de développement C/C++.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="b7bc8-119">Les programmeurs doivent être familiarisés avec les concepts de mise en réseau et le protocole RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="b7bc8-120">RADIUS est documenté dans le document [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) et [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="b7bc8-121">L’API Server Data Objects est conçue pour être utilisée par les programmeurs à l’aide du logiciel de développement C/C++ ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="b7bc8-122">Les programmeurs doivent être familiarisés avec le [service d’accès à distance](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) et le protocole RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b7bc8-123">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="b7bc8-123">Run-time requirements</span></span>

<span data-ttu-id="b7bc8-124">L’API des extensions NPS est prise en charge sur Windows Server 2008 avec l’installation du service Microsoft Commercial Internet (MCIS).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="b7bc8-125">L’API des objets de données du serveur est prise en charge sur Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="b7bc8-126">NPS est disponible sur Windows Server 2008 avec l’installation du service Microsoft Commercial Internet (MCIS).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b7bc8-127">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b7bc8-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b7bc8-128">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b7bc8-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="b7bc8-129">Informations générales concernant RADIUS, IAS et NPS.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="b7bc8-130">API des extensions du serveur NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="b7bc8-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="b7bc8-131">API d’implémentation des dll d’extension utilisées pour l’authentification, l’autorisation et la gestion des comptes.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="b7bc8-132">API des objets de données du serveur</span><span class="sxs-lookup"><span data-stu-id="b7bc8-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="b7bc8-133">API pour la gestion de la configuration de la stratégie réseau.</span><span class="sxs-lookup"><span data-stu-id="b7bc8-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="b7bc8-134">Programmabilité SQL</span><span class="sxs-lookup"><span data-stu-id="b7bc8-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="b7bc8-135">Exemples de procédures stockées utilisées pour la gestion de la journalisation NPS (IAS).</span><span class="sxs-lookup"><span data-stu-id="b7bc8-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b7bc8-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7bc8-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b7bc8-137">[TechNet : serveur NPS (Network Policy Server)](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="b7bc8-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="b7bc8-138">[TechNet : service d’authentification Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="b7bc8-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="b7bc8-139">Protection d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="b7bc8-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 