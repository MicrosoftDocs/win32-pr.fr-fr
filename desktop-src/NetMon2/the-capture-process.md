---
description: Le processus de capture est le même pour chacune des quatre interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Processus de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552297"
---
# <a name="the-capture-process"></a><span data-ttu-id="1de01-103">Processus de capture</span><span class="sxs-lookup"><span data-stu-id="1de01-103">The Capture Process</span></span>

<span data-ttu-id="1de01-104">Le processus de capture est le même pour chacune des quatre interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="1de01-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="1de01-105">Dans chaque cas, le processus comprend les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1de01-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="1de01-106">Obtention de l’objet d’interface NPP à utiliser</span><span class="sxs-lookup"><span data-stu-id="1de01-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="1de01-107">Connexion au réseau</span><span class="sxs-lookup"><span data-stu-id="1de01-107">Connecting to the network</span></span>
-   <span data-ttu-id="1de01-108">Démarrage, puis arrêt de la [ *capture*](c.md)</span><span class="sxs-lookup"><span data-stu-id="1de01-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="1de01-109">Déconnexion du réseau</span><span class="sxs-lookup"><span data-stu-id="1de01-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="1de01-110">Lorsque vous obtenez l’objet d’interface souhaité, veillez à appeler uniquement les méthodes incluses dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="1de01-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="1de01-111">L’illustration suivante montre que chaque interface fournit des méthodes similaires pour capturer les données réseau.</span><span class="sxs-lookup"><span data-stu-id="1de01-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="1de01-112">Une erreur est retournée si vous vous connectez au réseau avec une interface, puis essayez d’exécuter une capture à l’aide des méthodes d’une autre interface.</span><span class="sxs-lookup"><span data-stu-id="1de01-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="1de01-113">Les illustrations suivantes montrent deux façons différentes d’exécuter une capture.</span><span class="sxs-lookup"><span data-stu-id="1de01-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="1de01-114">La première illustration montre comment exécuter une ou plusieurs captures séquentielles, ce qui vous permet de créer n’importe quel nombre de captures indépendantes.</span><span class="sxs-lookup"><span data-stu-id="1de01-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![capture séquentielle](images/capt1.png)

<span data-ttu-id="1de01-116">Comme indiqué ci-dessus, une fois que vous êtes connecté au réseau, vous pouvez démarrer et arrêter une capture autant de fois que vous le souhaitez, en démarrant une nouvelle capture et en générant de nouvelles statistiques chaque fois que vous redémarrez la capture.</span><span class="sxs-lookup"><span data-stu-id="1de01-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="1de01-117">Par exemple, pour une capture différée à l’aide de l’interface [**IDelaydC**](idelaydc.md) , un nouveau [*fichier de capture*](c.md) est créé chaque fois que vous redémarrez la capture.</span><span class="sxs-lookup"><span data-stu-id="1de01-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="1de01-118">Toutefois, sachez également que chaque fois que vous redémarrez le processus de capture, vous devez appeler la méthode de configuration appropriée pour reconfigurer la connexion.</span><span class="sxs-lookup"><span data-stu-id="1de01-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="1de01-119">Pour l’appel initial de démarrage de la capture, la connexion est configurée par l’appel de la connexion au réseau.</span><span class="sxs-lookup"><span data-stu-id="1de01-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="1de01-120">La deuxième illustration montre comment vous pouvez exécuter une capture unique en suspendant et redémarrant.</span><span class="sxs-lookup"><span data-stu-id="1de01-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![capture unique en suspendant et redémarrant](images/capt2.png)

<span data-ttu-id="1de01-122">Dans ce cas, vous pouvez suspendre et redémarrer une capture autant de fois que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="1de01-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="1de01-123">Avec cette approche, vous pouvez exécuter une capture dont les données (et les statistiques associées) sont enregistrées sous la forme d’une capture unique.</span><span class="sxs-lookup"><span data-stu-id="1de01-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="1de01-124">Par exemple, pour effectuer une capture différée à l’aide de l’interface [**IDelaydC**](idelaydc.md) , toutes les informations réseau capturées sont enregistrées dans un [*fichier de capture*](c.md)unique.</span><span class="sxs-lookup"><span data-stu-id="1de01-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1de01-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1de01-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de01-126">**CreateNPPInterface**</span><span class="sxs-lookup"><span data-stu-id="1de01-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="1de01-127">**IDelaydC :: configure**</span><span class="sxs-lookup"><span data-stu-id="1de01-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="1de01-128">**IDelaydC :: Connect**</span><span class="sxs-lookup"><span data-stu-id="1de01-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="1de01-129">**IDelaydC ::D éconnecter**</span><span class="sxs-lookup"><span data-stu-id="1de01-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="1de01-130">**IDelaydC ::P ause**</span><span class="sxs-lookup"><span data-stu-id="1de01-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="1de01-131">**IDelaydC :: Resume**</span><span class="sxs-lookup"><span data-stu-id="1de01-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="1de01-132">**IDelaydC :: Start**</span><span class="sxs-lookup"><span data-stu-id="1de01-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="1de01-133">**IDelaydC :: Stop**</span><span class="sxs-lookup"><span data-stu-id="1de01-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="1de01-134">**IESP :: configure**</span><span class="sxs-lookup"><span data-stu-id="1de01-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="1de01-135">**IESP :: Connect**</span><span class="sxs-lookup"><span data-stu-id="1de01-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="1de01-136">**IESP ::D éconnecter**</span><span class="sxs-lookup"><span data-stu-id="1de01-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="1de01-137">**IESP ::P ause**</span><span class="sxs-lookup"><span data-stu-id="1de01-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="1de01-138">**IESP :: Resume**</span><span class="sxs-lookup"><span data-stu-id="1de01-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="1de01-139">**IESP :: Start**</span><span class="sxs-lookup"><span data-stu-id="1de01-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="1de01-140">**IESP :: Stop**</span><span class="sxs-lookup"><span data-stu-id="1de01-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="1de01-141">**IRTC :: configure**</span><span class="sxs-lookup"><span data-stu-id="1de01-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="1de01-142">**IRTC :: Connect**</span><span class="sxs-lookup"><span data-stu-id="1de01-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="1de01-143">**IRTC ::D éconnecter**</span><span class="sxs-lookup"><span data-stu-id="1de01-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="1de01-144">**IRTC ::P ause**</span><span class="sxs-lookup"><span data-stu-id="1de01-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="1de01-145">**IRTC :: Resume**</span><span class="sxs-lookup"><span data-stu-id="1de01-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="1de01-146">**IRTC :: Start**</span><span class="sxs-lookup"><span data-stu-id="1de01-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="1de01-147">**IRTC :: Stop**</span><span class="sxs-lookup"><span data-stu-id="1de01-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="1de01-148">**IStats :: configure**</span><span class="sxs-lookup"><span data-stu-id="1de01-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="1de01-149">**IStats :: Connect**</span><span class="sxs-lookup"><span data-stu-id="1de01-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="1de01-150">**IStats ::D éconnecter**</span><span class="sxs-lookup"><span data-stu-id="1de01-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="1de01-151">**IStats ::P ause**</span><span class="sxs-lookup"><span data-stu-id="1de01-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="1de01-152">**IStats :: Resume**</span><span class="sxs-lookup"><span data-stu-id="1de01-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="1de01-153">**IStats :: Start**</span><span class="sxs-lookup"><span data-stu-id="1de01-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="1de01-154">**IStats :: Stop**</span><span class="sxs-lookup"><span data-stu-id="1de01-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



