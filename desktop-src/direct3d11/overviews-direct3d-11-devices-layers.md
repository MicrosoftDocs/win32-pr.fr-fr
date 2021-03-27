---
title: Couches logicielles
description: Le runtime Direct3D 11 est construit avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs dans les couches externes. Cette section décrit les fonctionnalités de chaque couche.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507926"
---
# <a name="software-layers"></a><span data-ttu-id="d9bd3-104">Couches logicielles</span><span class="sxs-lookup"><span data-stu-id="d9bd3-104">Software Layers</span></span>

<span data-ttu-id="d9bd3-105">Le runtime Direct3D 11 est construit avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs dans les couches externes.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="d9bd3-106">Cette section décrit les fonctionnalités de chaque couche.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="d9bd3-107">En règle générale, les couches ajoutent des fonctionnalités, mais ne modifient pas le comportement existant.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="d9bd3-108">Par exemple, les fonctions de base auront les mêmes valeurs de retour que celles de la couche de débogage en cours d’instanciation, bien qu’une sortie de débogage supplémentaire puisse être fournie si la couche de débogage est instanciée.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="d9bd3-109">Pour créer des couches quand un appareil est créé, appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) et fournissez une ou plusieurs valeurs d’indicateur de [**\_ création d' \_ appareil \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .</span><span class="sxs-lookup"><span data-stu-id="d9bd3-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="d9bd3-110">Direct3D 11 fournit les couches de Runtime suivantes :</span><span class="sxs-lookup"><span data-stu-id="d9bd3-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="d9bd3-111">Couche principale</span><span class="sxs-lookup"><span data-stu-id="d9bd3-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="d9bd3-112">Couche de débogage</span><span class="sxs-lookup"><span data-stu-id="d9bd3-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="d9bd3-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9bd3-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="d9bd3-114">Couche principale</span><span class="sxs-lookup"><span data-stu-id="d9bd3-114">Core Layer</span></span>

<span data-ttu-id="d9bd3-115">La couche de base existe par défaut ; en fournissant un mappage très étroit entre l’API et le pilote de périphérique, ce qui minimise la surcharge des appels haute fréquence.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="d9bd3-116">Étant donné que la couche de base est essentielle pour les performances, elle effectue uniquement une validation critique.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="d9bd3-117">Les couches restantes sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="d9bd3-118">Couche de débogage</span><span class="sxs-lookup"><span data-stu-id="d9bd3-118">Debug Layer</span></span>

<span data-ttu-id="d9bd3-119">La couche de débogage fournit une validation de paramètres et de cohérence étendues supplémentaires (par exemple, la validation de la liaison de nuanceur et la liaison de ressources, la validation de la cohérence des paramètres et la création de rapports sur les erreurs).</span><span class="sxs-lookup"><span data-stu-id="d9bd3-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="d9bd3-120">Pour créer un appareil qui prend en charge la couche de débogage, vous devez installer le kit de développement logiciel (SDK) DirectX (pour obtenir D3D11SDKLayers.dll), puis spécifier l’indicateur de **\_ \_ \_ débogage d3d11 créer un appareil** lors de l’appel de la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou de la fonction [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) .</span><span class="sxs-lookup"><span data-stu-id="d9bd3-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="d9bd3-121">Si vous exécutez votre application avec la couche de débogage activée, l’application sera considérablement plus lente.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="d9bd3-122">Toutefois, pour vous assurer que votre application ne nettoie pas les erreurs et les avertissements avant de l’envoyer, utilisez la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="d9bd3-123">Pour plus d’informations, consultez [utilisation de la couche de débogage pour déboguer des applications](using-the-debug-layer-to-test-apps.md).</span><span class="sxs-lookup"><span data-stu-id="d9bd3-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="d9bd3-124">Pour Windows 7 avec la mise à jour de plateforme pour Windows 7 (KB2670838) ou Windows 8. x, pour créer un appareil qui prend en charge la couche de débogage, installez le kit de développement logiciel (SDK) Windows pour Windows 8. x afin d’obtenir D3D11 \_1SDKLayers.dll.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="d9bd3-125">Pour Windows 10, pour créer un appareil qui prend en charge la couche de débogage, activez la fonctionnalité facultative « outils graphiques ».</span><span class="sxs-lookup"><span data-stu-id="d9bd3-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="d9bd3-126">Accédez au panneau Paramètres, sous système, applications & fonctionnalités, gérer les fonctionnalités facultatives, ajouter une fonctionnalité, puis Rechercher « outils Graphics ».</span><span class="sxs-lookup"><span data-stu-id="d9bd3-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="d9bd3-127">Pour plus d’informations sur le débogage des applications DirectX à distance, consultez [débogage des applications DirectX à distance](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span><span class="sxs-lookup"><span data-stu-id="d9bd3-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="d9bd3-128">Vous pouvez également activer/désactiver l’indicateur de débogage à l’aide du [panneau de configuration DirectX](/previous-versions//bb219725(v=vs.85)) inclus dans le kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="d9bd3-129">Lorsque la couche de débogage répertorie les fuites de mémoire, elle génère une liste de pointeurs d’interface d’objet avec leurs noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="d9bd3-130">Le nom convivial par défaut est « sans &lt; nom &gt; ».</span><span class="sxs-lookup"><span data-stu-id="d9bd3-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="d9bd3-131">Vous pouvez définir le nom convivial à l’aide de la méthode [**ID3D11DeviceChild :: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) et du GUID **WKPDID \_ D3DDebugObjectName** qui se trouve dans D3Dcommon. h.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="d9bd3-132">Par exemple, pour nommer pTexture avec le nom de SDKLayer mytexture.jpg, utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d9bd3-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="d9bd3-133">En règle générale, vous devez compiler ces appels en dehors de votre version de production.</span><span class="sxs-lookup"><span data-stu-id="d9bd3-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9bd3-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9bd3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9bd3-135">Appareils</span><span class="sxs-lookup"><span data-stu-id="d9bd3-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 