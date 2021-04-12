---
description: Fournit l’accès aux événements de stylet provenant des numériseurs de stylet ou tactile.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Référence RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203811"
---
# <a name="realtimestylus-reference"></a><span data-ttu-id="eb62c-103">Référence RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="eb62c-103">RealTimeStylus Reference</span></span>

<span data-ttu-id="eb62c-104">Fournit l’accès aux événements de stylet provenant des numériseurs de stylet ou tactile.</span><span class="sxs-lookup"><span data-stu-id="eb62c-104">Provides access to the stylus events coming from pen or touch digitizers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb62c-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="eb62c-105">In This Section</span></span>

-   [<span data-ttu-id="eb62c-106">Classes et interfaces RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="eb62c-106">RealTimeStylus Classes and Interfaces</span></span>](realtimestylus-classes-and-interfaces.md)
-   [<span data-ttu-id="eb62c-107">Énumérations RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="eb62c-107">RealTimeStylus Enumerations</span></span>](realtimestylus-enumerations.md)
-   [<span data-ttu-id="eb62c-108">Structures RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="eb62c-108">RealTimeStylus Structures</span></span>](realtimestylus-structures.md)

## <a name="remarks"></a><span data-ttu-id="eb62c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="eb62c-109">Remarks</span></span>

<span data-ttu-id="eb62c-110">Cet objet implémente l’interface com [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .</span><span class="sxs-lookup"><span data-stu-id="eb62c-110">This object implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) COM interface.</span></span>

<span data-ttu-id="eb62c-111">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="eb62c-111">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="eb62c-112">Vous pouvez contrôler complètement, restituer dynamiquement, modifier et même supprimer des données du flux de paquets dans les plug-ins synchrones et asynchrones de l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="eb62c-112">You can fully control, dynamically render, modify, and even delete data from the packet stream within the synchronous and asynchronous plug-ins of the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span>

<span data-ttu-id="eb62c-113">Le stylet en temps réel permet de créer un objet **InkCollecting** qui est monothread et qui réside dans le thread d’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="eb62c-113">The real time stylus provides a way to create an **InkCollecting** object that is single-threaded and resident in the application UI thread.</span></span> <span data-ttu-id="eb62c-114">Cet objet **InkCollecting** accède aux données de stylet en temps réel à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="eb62c-114">This **InkCollecting** object accesses the real time stylus data from the queue.</span></span> <span data-ttu-id="eb62c-115">Un objet **InkCollecting** conjointement avec le stylet en temps réel permet la modification en temps réel de la sélection et l’édition en temps réel des données d’encre collectées.</span><span class="sxs-lookup"><span data-stu-id="eb62c-115">An **InkCollecting** object in conjunction with real time stylus enables real-time selection editing and real-time editing of the collected ink data.</span></span> <span data-ttu-id="eb62c-116">Pour plus d’informations, consultez [accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="eb62c-116">For more information, please see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span>

<span data-ttu-id="eb62c-117">Utilisez l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) pour interagir directement avec le flux de données du stylet de tablette ou pour bloquer l’encrage en temps réel.</span><span class="sxs-lookup"><span data-stu-id="eb62c-117">Use the [**RealTimeStylus Class**](realtimestylus-class.md) object to interact directly with the tablet stylus data stream or to block real-time inking.</span></span> <span data-ttu-id="eb62c-118">Utilisez l’objet de [**classe InkCollector**](inkcollector-class.md) , l’objet de [**classe InkOverlay**](inkoverlay-class.md) , le contrôle de [contrôle InkPicture](inkpicture-control-reference.md) ou le contrôle de [contrôle InkEdit](inkedit-control-reference.md) lorsque le comportement par défaut de ces objets fournit le comportement dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="eb62c-118">Use the [**InkCollector Class**](inkcollector-class.md) object, [**InkOverlay Class**](inkoverlay-class.md) object, [InkPicture Control](inkpicture-control-reference.md) control, or [InkEdit Control](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

<span data-ttu-id="eb62c-119">Les événements de stylet en temps réel se trouvent sur un handle de fenêtre spécifique dans un rectangle d’entrée de fenêtre spécifique.</span><span class="sxs-lookup"><span data-stu-id="eb62c-119">The real time stylus events are on a specific window handle within a specific window input rectangle.</span></span> <span data-ttu-id="eb62c-120">Le RealTimeStylusService peut envoyer des données de stylet à plusieurs objets de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="eb62c-120">The RealTimeStylusService can send stylus data to multiple [**RealTimeStylus Class**](realtimestylus-class.md) objects.</span></span> <span data-ttu-id="eb62c-121">Chaque objet de **classe RealTimeStylus** reçoit des données de stylet pour une section spécifique d’une fenêtre en fonction de la [**propriété IRealTimeStylus :: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) définie pour cet objet de **classe RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="eb62c-121">Each **RealTimeStylus Class** object receives stylus data for a specific section of a window based on the defined [**IRealTimeStylus::WindowInputRectangle Property**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) for that **RealTimeStylus Class** object.</span></span> <span data-ttu-id="eb62c-122">L’objet de **classe RealTimeStylus** obtient les données de stylet, puis les traite via une liste de plug-ins synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="eb62c-122">The **RealTimeStylus Class** object gets the stylus data and then processes this through a list of synchronous and asynchronous plug-ins.</span></span>

<span data-ttu-id="eb62c-123">La différence entre les plug-ins synchrones et les plug-ins asynchrones réside dans le thread dans lequel ils s’exécutent et dans la séquence d’appel.</span><span class="sxs-lookup"><span data-stu-id="eb62c-123">The difference between the synchronous plug-ins and the asynchronous plug-ins lies in the thread in which they execute and the calling sequence.</span></span> <span data-ttu-id="eb62c-124">Les plug-ins synchrones sont appelés par le thread dans lequel s’exécute l’objet de [**classe RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="eb62c-124">Synchronous plug-ins are called by the thread in which the [**RealTimeStylus Class**](realtimestylus-class.md) object executes.</span></span> <span data-ttu-id="eb62c-125">Chaque fois que l’objet de **classe RealTimeStylus** est instancié, un thread d’exécution est instancié.</span><span class="sxs-lookup"><span data-stu-id="eb62c-125">Every time **RealTimeStylus Class** object is instantiated, an execution thread is instantiated.</span></span> <span data-ttu-id="eb62c-126">Les plug-ins synchrones sont exécutés sur ce nouveau thread instancié pour l’instance de l’objet de **classe RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="eb62c-126">Synchronous plug-ins are executed on this new thread instantiated for the instance of the **RealTimeStylus Class** object.</span></span> <span data-ttu-id="eb62c-127">Les plug-ins asynchrones sont appelés par le biais du thread d’interface utilisateur ou d’application après que le flux de paquets a été traité par les plug-ins synchrones et stockés dans la file d’attente de sortie.</span><span class="sxs-lookup"><span data-stu-id="eb62c-127">Asynchronous plug-ins are called through the UI or application thread after the packet stream has been processed by the synchronous plug-ins and stored in the output queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb62c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb62c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb62c-129">**Interface IDynamicRenderer**</span><span class="sxs-lookup"><span data-stu-id="eb62c-129">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[<span data-ttu-id="eb62c-130">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="eb62c-130">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[<span data-ttu-id="eb62c-131">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="eb62c-131">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[<span data-ttu-id="eb62c-132">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="eb62c-132">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
