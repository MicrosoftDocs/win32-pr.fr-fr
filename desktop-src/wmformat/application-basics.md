---
title: Notions de base des applications
description: Notions de base des applications
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- SDK Windows Media format, notions de base des applications DRM
- gestion des droits numériques (DRM), principes de base des applications
- DRM (gestion des droits numériques), principes de base des applications
- gestion des droits numériques (DRM), fonction WMDRMStartup
- DRM (gestion des droits numériques), fonction WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190806"
---
# <a name="application-basics"></a><span data-ttu-id="b6022-109">Notions de base des applications</span><span class="sxs-lookup"><span data-stu-id="b6022-109">Application Basics</span></span>

<span data-ttu-id="b6022-110">Vous devez effectuer un traitement supplémentaire pour toutes les applications qui utilisent les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="b6022-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="b6022-111">Cette rubrique décrit la configuration requise pour une application simple.</span><span class="sxs-lookup"><span data-stu-id="b6022-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="b6022-112">Tout d’abord, vous devez initialiser les API étendues du client Windows Media DRM en appelant la fonction [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="b6022-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="b6022-113">Les objets du kit de développement logiciel (SDK) sont des objets COM, mais vous n’avez pas besoin d’appeler **CoIntialize**, car la fonction **WMDRMStatup** Initialise com pour vous.</span><span class="sxs-lookup"><span data-stu-id="b6022-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="b6022-114">Le kit de développement logiciel (SDK) du format Windows Media utilise uniquement un sous-ensemble de COM. par conséquent, si vous utilisez des objets COM autres que ceux de l’API étendue du client Windows Media DRM, vous devez toujours appeler **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="b6022-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="b6022-115">Tous les objets des API étendues du client Windows Media DRM sont créés à l’aide des fonctions et des méthodes d’assistance.</span><span class="sxs-lookup"><span data-stu-id="b6022-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="b6022-116">Vous n’avez jamais besoin d’appeler **CoCreateInstance** pour créer un objet.</span><span class="sxs-lookup"><span data-stu-id="b6022-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="b6022-117">La première interface à instancier pour toute application qui utilise le kit de développement logiciel (SDK) est [**IWMDRMProvider**](iwmdrmprovider.md), que vous pouvez utiliser pour instancier toutes les autres interfaces de base.</span><span class="sxs-lookup"><span data-stu-id="b6022-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="b6022-118">Pour récupérer une instance de **IWMDRMProvider**, vous devez appeler [**WMDRMCreateProvider**](wmdrmcreateprovider.md) ou [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span><span class="sxs-lookup"><span data-stu-id="b6022-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="b6022-119">La différence entre ces fonctions est que **WMDRMCreateProvider** crée un objet qui peut à son tour créer uniquement des objets qui ne prennent pas en charge les méthodes qui requièrent la bibliothèque stub.</span><span class="sxs-lookup"><span data-stu-id="b6022-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="b6022-120">Une fois que vous disposez d’une instance de **IWMDRMProvider**, vous pouvez créer les autres objets dont vous avez besoin en appelant [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="b6022-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="b6022-121">Lorsque vous êtes prêt à quitter votre application, vous devez libérer les ressources du sous-système DRM en appelant la fonction [**WMDRMShutdown**](wmdrmshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="b6022-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="b6022-122">Cette fonction arrête également COM pour vous.</span><span class="sxs-lookup"><span data-stu-id="b6022-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="b6022-123">L’exemple de code suivant montre comment initialiser et conclure une application qui utilise les API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="b6022-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a><span data-ttu-id="b6022-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6022-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6022-125">**Prise en main**</span><span class="sxs-lookup"><span data-stu-id="b6022-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




