---
description: La version 3,1 de l’interface de programmation d’applications de téléphonie (TAPI) Microsoft est une API COM (Component Object Model) qui fusionne les téléphonie classiques et IP.
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: Interface de programmation d’applications de téléphonie version 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535496"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="3d357-103">Interface de programmation d’applications de téléphonie version 3,1</span><span class="sxs-lookup"><span data-stu-id="3d357-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="3d357-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="3d357-104">Purpose</span></span>

<span data-ttu-id="3d357-105">La version 3,1 de l’interface de programmation d’applications de téléphonie (TAPI) Microsoft est une API COM (Component Object Model) qui fusionne les téléphonie classiques et IP.</span><span class="sxs-lookup"><span data-stu-id="3d357-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3d357-106">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="3d357-106">Where applicable</span></span>

<span data-ttu-id="3d357-107">Les applications TAPI possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d357-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="3d357-108">Vidéoconférence multidiffusion d’IP multimédia avec qualité de service (QOS)</span><span class="sxs-lookup"><span data-stu-id="3d357-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="3d357-109">Appels vocaux via Internet à l’aide du protocole H. 323</span><span class="sxs-lookup"><span data-stu-id="3d357-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="3d357-110">Applications de centre d’appels pouvant suivre plusieurs agents</span><span class="sxs-lookup"><span data-stu-id="3d357-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="3d357-111">Appels vocaux de base sur le réseau téléphonique public commuté (RTPC)</span><span class="sxs-lookup"><span data-stu-id="3d357-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="3d357-112">Contrôle PBX</span><span class="sxs-lookup"><span data-stu-id="3d357-112">PBX control</span></span>
-   <span data-ttu-id="3d357-113">Systèmes de réponse vocale interactive (IVR)</span><span class="sxs-lookup"><span data-stu-id="3d357-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="3d357-114">Messagerie vocale</span><span class="sxs-lookup"><span data-stu-id="3d357-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3d357-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="3d357-115">Developer audience</span></span>

<span data-ttu-id="3d357-116">Vous pouvez écrire des applications compatibles TAPI dans de nombreux langages, notamment Java, Visual Basic et C/C++.</span><span class="sxs-lookup"><span data-stu-id="3d357-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="3d357-117">Vous devez vous familiariser avec COM.</span><span class="sxs-lookup"><span data-stu-id="3d357-117">Familiarity with COM is required.</span></span> <span data-ttu-id="3d357-118">L’expérience de développement avec les télécommunications ou d’autres applications de téléphonie est utile, mais pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3d357-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3d357-119">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="3d357-119">Run-time requirements</span></span>

<span data-ttu-id="3d357-120">TAPI version 3,1 permet le développement d’applications de communication pour les systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3d357-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3d357-121">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3d357-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="3d357-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3d357-122">Topic</span></span></th><th><span data-ttu-id="3d357-123">Description</span><span class="sxs-lookup"><span data-stu-id="3d357-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="3d357-124"><a href="tapi-3-1-overview.md">Vue d'ensemble</a></span><span class="sxs-lookup"><span data-stu-id="3d357-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="3d357-125">Informations générales sur l’architecture et les composants TAPI.</span><span class="sxs-lookup"><span data-stu-id="3d357-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="3d357-126">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3d357-126">Reference</span></span><br/></td><td><span data-ttu-id="3d357-127">Documentation pour :</span><span class="sxs-lookup"><span data-stu-id="3d357-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="3d357-128"><a href="call-and-media-controls-reference.md">Référence des contrôles d’appel et de média</a></span><span class="sxs-lookup"><span data-stu-id="3d357-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="3d357-129"><a href="call-center-controls-reference.md">Référence des contrôles du centre d’appels</a></span><span class="sxs-lookup"><span data-stu-id="3d357-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="3d357-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Référence Rendezvous</a></span><span class="sxs-lookup"><span data-stu-id="3d357-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="3d357-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d357-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d357-132">Vue d’ensemble de la téléphonie Microsoft</span><span class="sxs-lookup"><span data-stu-id="3d357-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="3d357-133">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="3d357-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="3d357-134">Fournisseurs de services TAPI</span><span class="sxs-lookup"><span data-stu-id="3d357-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

