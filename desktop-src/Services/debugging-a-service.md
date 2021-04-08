---
description: Vous pouvez utiliser l’une des méthodes suivantes pour déboguer votre service.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Déboguer un service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750797"
---
# <a name="debugging-a-service"></a><span data-ttu-id="7ff4c-103">Déboguer un service</span><span class="sxs-lookup"><span data-stu-id="7ff4c-103">Debugging a Service</span></span>

<span data-ttu-id="7ff4c-104">Vous pouvez utiliser l’une des méthodes suivantes pour déboguer votre service.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="7ff4c-105">Utilisez votre débogueur pour déboguer le service pendant qu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="7ff4c-106">Tout d’abord, obtenez l’identificateur de processus (PID) du processus de service.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="7ff4c-107">Une fois que vous avez obtenu le PID, attachez-le au processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="7ff4c-108">Pour plus d’informations sur la syntaxe, consultez la documentation fournie avec votre débogueur.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="7ff4c-109">Appelez la fonction [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) pour appeler le débogueur pour le débogage juste-à-temps.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="7ff4c-110">Spécifiez un débogueur à utiliser lors du démarrage d’un programme.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="7ff4c-111">Pour ce faire, créez une clé nommée **Image File Execution Options** à l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="7ff4c-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="7ff4c-112">**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="7ff4c-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="7ff4c-113">Créez une sous-clé avec le même nom que votre service (par exemple, MYSERV.EXE).</span><span class="sxs-lookup"><span data-stu-id="7ff4c-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="7ff4c-114">Pour cette sous-clé, ajoutez une valeur de type **reg \_ SZ**, **débogueur** nommé.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="7ff4c-115">Utilisez le chemin d’accès complet au débogueur comme valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="7ff4c-116">Dans l’applet services du panneau de configuration, sélectionnez votre service, cliquez sur **démarrage** , puis activez **autoriser le service à interagir avec le bureau**.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="7ff4c-117">Le service doit être un service interactif, sinon le débogueur ne peut pas s’exécuter sur le bureau par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="7ff4c-118">Notez que cette technique n’est plus prise en charge à partir de Windows Vista, car tous les services sont exécutés dans une session réservée exclusivement aux services et ne prennent pas en charge l’affichage d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="7ff4c-119">Utilisez [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) pour enregistrer des informations.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="7ff4c-120">Pour déboguer le code d’initialisation d’un service à démarrage automatique, vous devez installer et exécuter temporairement le service en tant que service de démarrage à la demande.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="7ff4c-121">Parfois, il peut être nécessaire d’exécuter un service en tant qu’application console à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="7ff4c-122">Dans ce scénario, la fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) retourne une **erreur \_ échec \_ de \_ \_ connexion du contrôleur de service**.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="7ff4c-123">Par conséquent, veillez à structurer votre code de façon à ce que le code propre au service ne soit pas appelé lorsque cette erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ff4c-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ff4c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ff4c-125">Débogage d’une application de service</span><span class="sxs-lookup"><span data-stu-id="7ff4c-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="7ff4c-126">Outils de débogage pour Windows</span><span class="sxs-lookup"><span data-stu-id="7ff4c-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
