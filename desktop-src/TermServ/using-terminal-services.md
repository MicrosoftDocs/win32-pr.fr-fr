---
title: Utilisation de Services Bureau à distance
description: Comment programmer dans l’environnement Services Bureau à distance et comment étendre la technologie Services Bureau à distance (anciennement appelée services Terminal Server) au Web à l’aide de Connexion Bureau à distance par le Web.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106540750"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="5cfd3-104">Utilisation de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfd3-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="5cfd3-105">Les sections suivantes décrivent comment programmer dans l’environnement Services Bureau à distance et comment étendre la technologie Services Bureau à distance (anciennement appelée services Terminal Server) au Web à l’aide de Connexion Bureau à distance par le Web.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="5cfd3-106">Si vous recherchez des informations sur l’utilisateur pour les connexions Bureau à distance, consultez [se connecter à un autre ordinateur à l’aide de connexion Bureau à distance](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span><span class="sxs-lookup"><span data-stu-id="5cfd3-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="5cfd3-107">Cette rubrique est destinée aux développeurs de logiciels.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="5cfd3-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5cfd3-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5cfd3-109">Détection de l’installation du rôle Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfd3-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="5cfd3-110">Exemple de code C# qui montre une méthode qui retourne la **valeur true** si le rôle serveur services Bureau à distance est installé et en cours d’exécution ou **false** dans le cas contraire, à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-111">Extension de session Broker des services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="5cfd3-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="5cfd3-112">Vous pouvez étendre session Broker TS à l’aide de l’interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) com.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-113">Implémentation d’un énumérateur de point de terminaison audio personnalisé</span><span class="sxs-lookup"><span data-stu-id="5cfd3-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="5cfd3-114">À partir de Windows Server 2008 R2, vous pouvez implémenter un énumérateur de point de terminaison audio distant personnalisé dans le cadre d’un fournisseur de protocole Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-115">Monikers de session</span><span class="sxs-lookup"><span data-stu-id="5cfd3-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="5cfd3-116">DCOM (Distributed COM) permet l’activation d’objets pour chaque session à l’aide d’un moniker de session fourni par le système.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-117">Utilisation de l’extension ADSI pour Services Bureau à distance Configuration utilisateur</span><span class="sxs-lookup"><span data-stu-id="5cfd3-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="5cfd3-118">L’administration des propriétés utilisateur spécifiques à Services Bureau à distance est possible en utilisant les méthodes implémentées par l’extension ADSI (Active Directory Service Interfaces), qui est empaquetée avec la bibliothèque de liens dynamiques Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-119">Utilisation de l’API Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfd3-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="5cfd3-120">Décrit comment vous pouvez utiliser l’API Services Bureau à distance pour permettre aux applications d’effectuer des tâches dans un environnement Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-121">Utilisation de l’API de virtualisation Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfd3-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="5cfd3-122">Les développeurs peuvent utiliser cette API pour personnaliser la logique que Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) utilise pour déterminer la destination la plus appropriée pour une connexion cliente entrante.</span><span class="sxs-lookup"><span data-stu-id="5cfd3-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5cfd3-123">Interface WSDL pour les solutions VDI personnalisées</span><span class="sxs-lookup"><span data-stu-id="5cfd3-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="5cfd3-124">Les développeurs peuvent créer des services Web personnalisés qui gèrent les solutions VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="5cfd3-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="5cfd3-125">Pour plus d’informations, consultez [services Bureau à distance les instructions de programmation](terminal-services-programming-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="5cfd3-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cfd3-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5cfd3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cfd3-127">Les services Terminal Server sont désormais Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfd3-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="5cfd3-128">Détection de l’environnement de Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="5cfd3-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




