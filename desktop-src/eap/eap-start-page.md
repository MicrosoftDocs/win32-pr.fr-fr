---
title: Protocole EAP (Extensible Authentication Protocol)
description: Le protocole EAP (Extensible Authentication Protocol) est un standard pris en charge par plusieurs composants système. EAP est essentiel pour la protection de la sécurité des réseaux locaux sans fil (802.1 X) et des réseaux locaux câblés, des accès à distance et des réseaux privés virtuels (VPN).
ms.assetid: bdbac41e-064c-445f-8f86-a6e2eff2a683
keywords:
- Protocole EAP (Extensible Authentication Protocol)
- Protocole EAP (Extensible Authentication Protocol), page de démarrage
- Protocole EAP
- EAP, voir protocole EAP (Extensible Authentication Protocol)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79b9585363d74eb50190d0fd6355830a7087aa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724940"
---
# <a name="extensible-authentication-protocol"></a><span data-ttu-id="405f1-108">Protocole EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="405f1-108">Extensible Authentication Protocol</span></span>

## <a name="purpose"></a><span data-ttu-id="405f1-109">Objectif</span><span class="sxs-lookup"><span data-stu-id="405f1-109">Purpose</span></span>

<span data-ttu-id="405f1-110">Le protocole EAP (Extensible Authentication Protocol) est un standard pris en charge par plusieurs composants système.</span><span class="sxs-lookup"><span data-stu-id="405f1-110">The Extensible Authentication Protocol (EAP) is a standard supported by several system components.</span></span> <span data-ttu-id="405f1-111">EAP est essentiel pour la protection de la sécurité des réseaux locaux sans fil (802.1 X) et des réseaux locaux câblés, des accès à distance et des réseaux privés virtuels (VPN).</span><span class="sxs-lookup"><span data-stu-id="405f1-111">EAP is crucial for protecting the security of wireless (802.1X) and wired LANs, Dial-up, and Virtual Private Networks (VPNs).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="405f1-112">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="405f1-112">Where applicable</span></span>

<span data-ttu-id="405f1-113">EAP améliore les protocoles d’authentification précédents, tels que le protocole PAP (Password Authentication Protocol) et le protocole CHAP (Challenge Handshake Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="405f1-113">EAP improves on previous authentication protocols such as Password Authentication Protocol (PAP) and Challenge Handshake Authentication Protocol (CHAP).</span></span>

<span data-ttu-id="405f1-114">Pour le développement de nouvelles méthodes EAP, consultez la page [Extensible Authentication Protocol Host](../eaphost/portal.md).</span><span class="sxs-lookup"><span data-stu-id="405f1-114">For new EAP method development, see [Extensible Authentication Protocol Host](../eaphost/portal.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="405f1-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="405f1-115">Developer audience</span></span>

<span data-ttu-id="405f1-116">L’API EAP est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="405f1-116">The EAP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="405f1-117">Les programmeurs doivent être familiarisés avec les concepts de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="405f1-117">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="405f1-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="405f1-118">Run-time requirements</span></span>

<span data-ttu-id="405f1-119">EAP est pris en charge sur les ordinateurs clients et serveurs qui s’exécutent sur Windows 2000 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="405f1-119">EAP is supported on client and server computers running on  Windows 2000 and later.</span></span> <span data-ttu-id="405f1-120">EAP est également pris en charge sur les ordinateurs qui exécutent Windows 2000 Server et versions ultérieures s’ils exécutent le service d’authentification Internet (IAS).</span><span class="sxs-lookup"><span data-stu-id="405f1-120">EAP is also supported on computers running on Windows 2000 Server and later if they are running Internet Authentication Service (IAS).</span></span> <span data-ttu-id="405f1-121">Pour plus d’informations sur les systèmes d’exploitation pris en charge, consultez la section relative à la configuration requise dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="405f1-121">For more information about supported operating systems, see the Requirements section in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="405f1-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="405f1-122">Related topics</span></span>

<dl> <span data-ttu-id="405f1-123"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="405f1-123"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="405f1-124">Service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="405f1-124">Remote Access Service</span></span>](/windows/desktop/RRAS/remote-access-start-page)
<span data-ttu-id="405f1-125"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="405f1-125"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="405f1-126">Service d'authentification Internet</span><span class="sxs-lookup"><span data-stu-id="405f1-126">Internet Authentication Service</span></span>](/windows/desktop/Nps/ias-extensions)
<span data-ttu-id="405f1-127"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="405f1-127"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="405f1-128">Utilisation du protocole EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="405f1-128">Using Extensible Authentication Protocol</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
<span data-ttu-id="405f1-129"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="405f1-129"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="405f1-130">Référence du protocole EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="405f1-130">Extensible Authentication Protocol Reference</span></span>](extensible-authentication-protocol-reference.md)
</dt> </dl>

 

 