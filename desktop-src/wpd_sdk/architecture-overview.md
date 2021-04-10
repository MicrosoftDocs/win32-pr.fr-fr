---
description: Présentation de l'architecture
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Présentation de l'architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868270"
---
# <a name="architecture-overview"></a><span data-ttu-id="6c4b9-103">Présentation de l'architecture</span><span class="sxs-lookup"><span data-stu-id="6c4b9-103">Architecture Overview</span></span>

<span data-ttu-id="6c4b9-104">L’architecture WPD peut être divisée en trois processus.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="6c4b9-105">Ces processus sont les trois composants principaux d’WPD : l’API, le sérialiseur et le pilote.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="6c4b9-106">L’illustration suivante représente les processus et les composants qui constituent l’architecture WPD.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![illustration illustrant les composants API, sérialiseur et pilote d’wpd](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="6c4b9-108">Interface de programmation d’applications WPD</span><span class="sxs-lookup"><span data-stu-id="6c4b9-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="6c4b9-109">L’API WPD est implémentée en tant que serveur COM in-proc.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="6c4b9-110">L’API utilise des API Microsoft Win32 standard pour communiquer avec le pilote WPD approprié.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="6c4b9-111">Un composant appelé sérialiseur WPD est utilisé par les objets d’API et le pilote pour regrouper ou décompresser des paramètres vers ou depuis Windows Driver Foundation (WDF)-mémoires tampons de l’infrastructure de pilote de mode utilisateur (UMDF).</span><span class="sxs-lookup"><span data-stu-id="6c4b9-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="6c4b9-112">Sérialiseur WPD</span><span class="sxs-lookup"><span data-stu-id="6c4b9-112">The WPD Serializer</span></span>

<span data-ttu-id="6c4b9-113">Le sérialiseur WPD est implémenté en tant que serveur COM in-proc.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="6c4b9-114">L’API WPD utilise le sérialiseur pour compresser les commandes et les paramètres dans les tampons de messages envoyés au pilote.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="6c4b9-115">Le pilote utilise le sérialiseur pour décompresser les tampons de messages en vue de leur traitement.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="6c4b9-116">Le pilote utilise également le sérialiseur pour compresser les données et les paramètres dans les tampons de réponse qui sont retournés à l’API WPD, et l’API WPD utilise le sérialiseur pour décompresser ces tampons de réponse pour revenir aux appelants.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="6c4b9-117">Pilote WPD</span><span class="sxs-lookup"><span data-stu-id="6c4b9-117">WPD Driver</span></span>

<span data-ttu-id="6c4b9-118">Le pilote WPD est implémenté en tant que pilote WDF (Windows Driver Foundation) standard (UMDF).</span><span class="sxs-lookup"><span data-stu-id="6c4b9-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="6c4b9-119">Les pilotes WPD sont hébergés par UMDF dans un processus distinct appelé hôte de pilote.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="6c4b9-120">Le pilote reçoit des messages du réflecteur UMDF (cela n’est pas indiqué dans le diagramme, car la manière dont les tampons sont reçus n’a pas d’importance pour le pilote.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="6c4b9-121">Pour plus d’informations, consultez la documentation UMDF.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="6c4b9-122">Le pilote implémente un gestionnaire de code de contrôle d’e/s (IOCL) spécifique à WPD pour traiter les messages WPD reçus par l’API WPD.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="6c4b9-123">Le pilote utilise le sérialiseur WPD pour décompresser des commandes et des paramètres à partir de ces mémoires tampons de messages, et pour empaqueter la réponse dans la mémoire tampon de retour.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="6c4b9-124">Les pilotes WPD peuvent communiquer avec leurs appareils en passant par un pilote en mode noyau, généralement accessible via les opérations de fichier Win32 (c’est-à-dire, CreateFile, ReadFile, WriteFile, etc.).</span><span class="sxs-lookup"><span data-stu-id="6c4b9-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="6c4b9-125">Pour les bus courants, Microsoft fournira des pilotes de noyau standard que les fournisseurs pourront utiliser, ce qui permettra aux fournisseurs d’envoyer une solution de pilote en mode utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="6c4b9-126">En outre, pour les appareils MTP (Media Transfer Protocol) et MSC (Storage-Class), Microsoft fournira des pilotes de classe WPD.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="6c4b9-127">Pour plus d’informations sur les pilotes WPD, consultez la documentation du pilote des appareils mobiles Windows dans le kit de pilotes Windows.</span><span class="sxs-lookup"><span data-stu-id="6c4b9-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c4b9-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c4b9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c4b9-129">**Vue d’ensemble de l’application**</span><span class="sxs-lookup"><span data-stu-id="6c4b9-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



