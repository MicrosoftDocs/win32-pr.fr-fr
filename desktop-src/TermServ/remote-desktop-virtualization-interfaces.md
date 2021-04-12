---
title: Bureau à distance les interfaces de virtualisation
description: L’API de virtualisation Bureau à distance prend en charge les interfaces suivantes.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315738"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="d590f-103">Bureau à distance les interfaces de virtualisation</span><span class="sxs-lookup"><span data-stu-id="d590f-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="d590f-104">L’API de virtualisation Bureau à distance prend en charge les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="d590f-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d590f-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d590f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d590f-106">**ITsSbBaseNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="d590f-107">Expose des méthodes qui signalent des messages d’État et d’erreur à Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="d590f-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-108">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="d590f-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="d590f-109">Expose des méthodes et des propriétés qui stockent des informations d’État sur une demande de connexion entrante à partir d’un client Connexion Bureau à distance (RDC).</span><span class="sxs-lookup"><span data-stu-id="d590f-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-110">**ITsSbClientConnectionPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d590f-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="d590f-111">Peut être utilisé pour définir les propriétés personnalisées d’une connexion cliente, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d590f-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-112">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d590f-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="d590f-113">Expose des méthodes et des propriétés qui contiennent des informations sur l’environnement qui héberge l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="d590f-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="d590f-114">Cette interface peut être utilisée pour stocker des informations sur un serveur physique qui héberge des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="d590f-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-115">**ITsSbEnvironmentPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d590f-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="d590f-116">Peut être utilisé pour définir les propriétés personnalisées d’un environnement qui héberge les ordinateurs cibles, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d590f-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-117">**ITsSbFilterPluginStore**</span><span class="sxs-lookup"><span data-stu-id="d590f-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="d590f-118">Filtrer le magasin de plug-ins</span><span class="sxs-lookup"><span data-stu-id="d590f-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-119">**ITsSbGenericNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-120">Expose les méthodes qui signalent l’achèvement à et obtient le temps d’attente du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-121">**ITsSbGlobalStore**</span><span class="sxs-lookup"><span data-stu-id="d590f-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="d590f-122">Expose les méthodes qui interrogent les ordinateurs cibles, les sessions, les environnements et les batteries de serveurs qui ont été ajoutés au magasin du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-123">**ITsSbLoadBalanceResult**</span><span class="sxs-lookup"><span data-stu-id="d590f-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="d590f-124">Expose des méthodes et des propriétés qui stockent le nom cible retourné par un algorithme d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="d590f-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-125">**ITsSbLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="d590f-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="d590f-126">Expose des méthodes que vous pouvez utiliser pour fournir un algorithme d’équilibrage de charge personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d590f-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-127">**ITsSbLoadBalancingNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-128">Expose les méthodes qui retournent le résultat d’un algorithme d’équilibrage de charge au service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-129">**ITsSbOrchestration**</span><span class="sxs-lookup"><span data-stu-id="d590f-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="d590f-130">Expose les méthodes utilisées par le Service Broker pour les connexions Bureau à distance pour s’assurer que la cible est prête avant qu’un client lui soit redirigé.</span><span class="sxs-lookup"><span data-stu-id="d590f-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-131">**ITsSbOrchestrationNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-132">Expose des méthodes qui retournent un objet [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) à Service Broker pour les connexions Bureau à distance après la préparation de la cible pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="d590f-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-133">**ITsSbPlacement**</span><span class="sxs-lookup"><span data-stu-id="d590f-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="d590f-134">Expose des méthodes qui préparent l’environnement (l’ordinateur qui héberge l’ordinateur virtuel).</span><span class="sxs-lookup"><span data-stu-id="d590f-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-135">**ITsSbPlacementNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-136">Expose des méthodes qui retournent des informations sur les environnements au service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-137">**ITsSbPlugin**</span><span class="sxs-lookup"><span data-stu-id="d590f-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="d590f-138">Expose les méthodes qui initialisent et terminent les plug-ins.</span><span class="sxs-lookup"><span data-stu-id="d590f-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-139">**ITsSbPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-140">Expose des méthodes qui notifient l’initialisation ou l’arrêt d’un plug-in par le Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-141">**ITsSbPluginPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d590f-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="d590f-142">Peut être utilisé pour définir les propriétés de plug-in personnalisées, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d590f-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-143">**ITsSbPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d590f-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="d590f-144">Peut être utilisé pour définir les propriétés personnalisées appropriées.</span><span class="sxs-lookup"><span data-stu-id="d590f-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-145">**ITsSbProvider**</span><span class="sxs-lookup"><span data-stu-id="d590f-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="d590f-146">Expose des méthodes qui créent des implémentations par défaut des objets utilisés dans Bureau à distance virtualisation.</span><span class="sxs-lookup"><span data-stu-id="d590f-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-147">**ITsSbProvisioning**</span><span class="sxs-lookup"><span data-stu-id="d590f-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="d590f-148">Expose des méthodes qui créent et gèrent des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="d590f-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-149">**ITsSbProvisioningPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-150">Expose des méthodes qui notifient le Service Broker pour les connexions Bureau à distance de la configuration des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="d590f-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-151">**ITsSbResourceNotification**</span><span class="sxs-lookup"><span data-stu-id="d590f-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="d590f-152">Expose les méthodes que le Service Broker pour les connexions Bureau à distance utilise pour notifier les plug-ins des modifications d’État qui se produisent dans la session, la cible et les objets de connexion client.</span><span class="sxs-lookup"><span data-stu-id="d590f-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-153">**ITsSbResourceNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="d590f-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="d590f-154">Expose les méthodes que le Service Broker pour les connexions Bureau à distance utilise pour notifier les plug-ins des modifications d’État qui se produisent dans la session, la cible et les objets de connexion client.</span><span class="sxs-lookup"><span data-stu-id="d590f-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-155">**ITsSbResourcePlugin**</span><span class="sxs-lookup"><span data-stu-id="d590f-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="d590f-156">Expose des méthodes qui étendent les fonctionnalités du Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-157">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="d590f-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="d590f-158">Expose des méthodes qui permettent aux plug-ins de ressources de stocker des objets tels que des sessions et des cibles.</span><span class="sxs-lookup"><span data-stu-id="d590f-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-159">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="d590f-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="d590f-160">Expose des méthodes qui permettent aux plug-ins de ressources de stocker des objets tels que des sessions et des cibles.</span><span class="sxs-lookup"><span data-stu-id="d590f-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-161">**ITsSbServiceNotification**</span><span class="sxs-lookup"><span data-stu-id="d590f-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="d590f-162">Expose les méthodes que le Service Broker pour les connexions Bureau à distance utilise pour notifier les plug-ins des modifications d’État qui se produisent dans le Service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-163">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="d590f-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="d590f-164">Expose les propriétés qui stockent des informations sur une session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d590f-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-165">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="d590f-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="d590f-166">Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.</span><span class="sxs-lookup"><span data-stu-id="d590f-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-167">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="d590f-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="d590f-168">Expose les propriétés qui stockent les informations de configuration et d’état d’une cible.</span><span class="sxs-lookup"><span data-stu-id="d590f-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-169">**ITsSbTargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d590f-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="d590f-170">Dérivez de cette interface pour définir un jeu de propriétés cible personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d590f-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-171">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="d590f-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="d590f-172">Expose les propriétés que le Service Broker de Connexion Bureau à distance utilise pour définir la file d’attente d’un plug-in.</span><span class="sxs-lookup"><span data-stu-id="d590f-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-173">**ITsSbTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="d590f-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="d590f-174">Expose des méthodes qui mettent à jour la file d’attente des tâches pour les plug-ins Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="d590f-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-175">**ITsSbTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="d590f-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="d590f-176">Expose des méthodes qui signalent des messages d’État et d’erreur sur les tâches au service Broker pour les connexions Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d590f-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="d590f-177">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="d590f-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="d590f-178">Permet d’étendre les fonctionnalités de session Broker TS (session Broker TS).</span><span class="sxs-lookup"><span data-stu-id="d590f-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="d590f-179">Implémentez cette interface lorsque vous souhaitez fournir un plug-in qui remplace la logique de redirection de session Broker TS.</span><span class="sxs-lookup"><span data-stu-id="d590f-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 