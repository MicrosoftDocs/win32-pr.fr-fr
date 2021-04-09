---
description: Les fournisseurs, sauf s’ils sont des fournisseurs découplés qui s’exécutent dans une application, sont chargés dans un Wmiprvse.exe processus, et non par le biais d' Svchost.exe avec un processus de Winmgmt.exe. Pour plus d’informations, consultez Hébergement et sécurité du fournisseur.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Fournisseurs de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951626"
---
# <a name="debugging-providers"></a><span data-ttu-id="26ac3-104">Fournisseurs de débogage</span><span class="sxs-lookup"><span data-stu-id="26ac3-104">Debugging Providers</span></span>

<span data-ttu-id="26ac3-105">Les fournisseurs, sauf s’ils sont des [*fournisseurs découplés*](gloss-d.md) qui s’exécutent dans une application, sont chargés dans un Wmiprvse.exe processus, et non par le biais d' Svchost.exe avec un processus de Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="26ac3-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="26ac3-106">Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="26ac3-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="26ac3-107">Lors de l’arrêt à un point d’arrêt, le débogueur Visual Studio fige l’intégralité du processus hôte du fournisseur, qui est généralement l’hôte partagé Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="26ac3-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="26ac3-108">Cela empêche le fonctionnement de tous les autres composants hébergés dans ce processus, y compris l’extension de Explorateur de serveurs WMI.</span><span class="sxs-lookup"><span data-stu-id="26ac3-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="26ac3-109">Les applications clientes qui appellent le fournisseur sont également bloquées.</span><span class="sxs-lookup"><span data-stu-id="26ac3-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="26ac3-110">Les problèmes qui se produisent sont moins graves dans Windows 2000 et les versions antérieures, car le fournisseur est chargé dans le processus de service WMI (Winmgmt.exe).</span><span class="sxs-lookup"><span data-stu-id="26ac3-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="26ac3-111">Si vous exécutez WMI Explorateur de serveurs dans une autre instance, l’IDE de Visual Studio ne se fige pas et vous pouvez libérer le point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="26ac3-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="26ac3-112">Il est recommandé d’exécuter votre fournisseur dans un processus d’hébergement distinct au cours de la phase de développement, afin que l’arrêt à un point d’arrêt bloque uniquement le processus qui héberge votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="26ac3-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="26ac3-113">Les autres fonctions de WMI restent accessibles aux Explorateur de serveurs WMI et à d’autres applications ou scripts basés sur WMI.</span><span class="sxs-lookup"><span data-stu-id="26ac3-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="26ac3-114">En outre, si votre fournisseur tombe en panne, il n’affecte pas le fonctionnement des autres fournisseurs chargés dans le même processus hôte.</span><span class="sxs-lookup"><span data-stu-id="26ac3-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="26ac3-115">Pour que votre fournisseur se charge dans son propre processus hôte, modifiez l’inscription du fournisseur pour définir la propriété [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) sur, `NetworkServiceHost:[MyProvider]` où MyProvider peut être toute chaîne qui identifie de façon unique votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="26ac3-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="26ac3-116">Par exemple, utilisez la valeur **\_ \_ Win32Provider. CLSID** .</span><span class="sxs-lookup"><span data-stu-id="26ac3-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="26ac3-117">Lorsque votre fournisseur est prêt à être expédié, retournez **\_ \_ Win32Provider. HostingModel** à la valeur prévue, par exemple **NetworkServiceHost**.</span><span class="sxs-lookup"><span data-stu-id="26ac3-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="26ac3-118">Si vous n’êtes pas en train de déboguer le chargement du fournisseur, vous pouvez appeler la [**méthode Load de la \_ classe des fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) pour forcer le chargement de votre fournisseur, puis l’attacher au processus de Wmiprvse.exe qui a chargé la dll et déboguer en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="26ac3-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26ac3-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26ac3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ac3-120">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="26ac3-120">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="26ac3-121">Classes de résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="26ac3-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
