---
description: L’interface de programmation d’applications de téléphonie (TAPI) Microsoft, version 2,2 (TAPI/C) permet l’implémentation d’applications de communication allant du contrôle de modem de base aux centres d’appel avec plusieurs agents et commutateurs.
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: Interface de programmation d’applications de téléphonie version 2,2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203168"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="3e5f5-103">Interface de programmation d’applications de téléphonie version 2,2</span><span class="sxs-lookup"><span data-stu-id="3e5f5-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="3e5f5-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="3e5f5-104">Purpose</span></span>

<span data-ttu-id="3e5f5-105">L’interface de programmation d’applications de téléphonie (TAPI) Microsoft, version 2,2 (TAPI/C) permet l’implémentation d’applications de communication allant du contrôle de modem de base aux centres d’appel avec plusieurs agents et commutateurs.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3e5f5-106">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="3e5f5-106">Where applicable</span></span>

<span data-ttu-id="3e5f5-107">Les applications TAPI 2,2 possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e5f5-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="3e5f5-108">Appels vocaux de base sur le réseau téléphonique public commuté (RTPC)</span><span class="sxs-lookup"><span data-stu-id="3e5f5-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="3e5f5-109">Applications de centre d’appels pour le suivi de plusieurs agents</span><span class="sxs-lookup"><span data-stu-id="3e5f5-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="3e5f5-110">Contrôle de modem</span><span class="sxs-lookup"><span data-stu-id="3e5f5-110">Modem control</span></span>
-   <span data-ttu-id="3e5f5-111">Contrôle PBX</span><span class="sxs-lookup"><span data-stu-id="3e5f5-111">PBX control</span></span>
-   <span data-ttu-id="3e5f5-112">Systèmes de réponse vocale interactive (IVR)</span><span class="sxs-lookup"><span data-stu-id="3e5f5-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="3e5f5-113">Messagerie vocale</span><span class="sxs-lookup"><span data-stu-id="3e5f5-113">Voice mail</span></span>
-   <span data-ttu-id="3e5f5-114">Contrôle détaillé de l’appareil téléphonique</span><span class="sxs-lookup"><span data-stu-id="3e5f5-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3e5f5-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="3e5f5-115">Developer audience</span></span>

<span data-ttu-id="3e5f5-116">TAPI/C est conçu pour être utilisé par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="3e5f5-117">L’expérience de développement avec les télécommunications ou d’autres applications de téléphonie est utile, mais pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3e5f5-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="3e5f5-118">Run-time requirements</span></span>

<span data-ttu-id="3e5f5-119">TAPI version 2,2 permet le développement d’applications de communication pour les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98 et Windows 95.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="3e5f5-120">Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, consultez la section Configuration requise de la documentation relative à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e5f5-121">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3e5f5-121">In this section</span></span>



| <span data-ttu-id="3e5f5-122">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3e5f5-122">Topic</span></span>                                          | <span data-ttu-id="3e5f5-123">Description</span><span class="sxs-lookup"><span data-stu-id="3e5f5-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e5f5-124">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="3e5f5-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="3e5f5-125">Informations générales sur l’architecture et les composants TAPI.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="3e5f5-126">Référence</span><span class="sxs-lookup"><span data-stu-id="3e5f5-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="3e5f5-127">Documentation des fonctions, structures, messages, constantes et classes d’appareils disponibles dans TAPI 2,2.</span><span class="sxs-lookup"><span data-stu-id="3e5f5-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3e5f5-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e5f5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e5f5-129">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3e5f5-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="3e5f5-130">Fournisseurs de services TAPI</span><span class="sxs-lookup"><span data-stu-id="3e5f5-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

