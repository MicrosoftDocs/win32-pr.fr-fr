---
title: Exemple de fournisseur de services
description: Exemple de fournisseur de services
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Gestionnaire de périphériques Windows Media, exemples
- Gestionnaire de périphériques, exemples
- Windows Media Gestionnaire de périphériques, exemple de fournisseur de services
- Gestionnaire de périphériques, exemple de fournisseur de services
- fournisseurs de services, exemples
- exemples, fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510825"
---
# <a name="sample-service-provider"></a><span data-ttu-id="c78d3-109">Exemple de fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="c78d3-109">Sample Service Provider</span></span>

<span data-ttu-id="c78d3-110">Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques comprend un exemple de fournisseur de services que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="c78d3-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="c78d3-111">Ce fournisseur de services comprend une classe qui signale chaque disque dur de l’ordinateur comme s’il s’agissait d’un appareil attaché.</span><span class="sxs-lookup"><span data-stu-id="c78d3-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="c78d3-112">La seule application qui utilisera ce fournisseur de services est l’exemple d’application ; L’Explorateur Windows ne voit pas les « périphériques » signalés par ce fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="c78d3-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="c78d3-113">L’exemple de fournisseur de services est un objet COM basé sur ATL.</span><span class="sxs-lookup"><span data-stu-id="c78d3-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="c78d3-114">Les étapes suivantes expliquent comment utiliser l’exemple de fournisseur de services :</span><span class="sxs-lookup"><span data-stu-id="c78d3-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="c78d3-115">L’exemple de fournisseur de services implémente très peu de fonctionnalités. il ne doit donc pas être utilisé pour tester les applications Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="c78d3-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="c78d3-116">Pour tester une application, utilisez un fournisseur de services entièrement implémenté.</span><span class="sxs-lookup"><span data-stu-id="c78d3-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="c78d3-117">L’exemple a été fourni avec une erreur de codage qui entraînera un dysfonctionnement du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="c78d3-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="c78d3-118">Pour corriger cette erreur, ouvrez le fichier MDSPEnumStorage. cpp installé dans le dossier < *chemin d’installation du kit de développement logiciel (SDK)*  > \\ WMFSDK95 \\ WMDM \\ MDSP \\ mshdsp, accédez à la ligne 185, puis modifiez la ligne suivante :</span><span class="sxs-lookup"><span data-stu-id="c78d3-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="c78d3-119">Par ceci :</span><span class="sxs-lookup"><span data-stu-id="c78d3-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="c78d3-120">Compilez le fichier MsHDSP.dll.</span><span class="sxs-lookup"><span data-stu-id="c78d3-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="c78d3-121">Pour ce faire, vous pouvez utiliser NMAKE ou Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c78d3-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="c78d3-122">Consultez [compilation de l’exemple de fournisseur de services à l’aide de NMAKE](compiling-the-sample-service-provider-using-nmake.md) ou [compilation de l’exemple de fournisseur de services à l’aide de Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) pour savoir comment compiler l’application.</span><span class="sxs-lookup"><span data-stu-id="c78d3-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="c78d3-123">Inscrivez MsHDSP.dll à l’aide de regsvr32.</span><span class="sxs-lookup"><span data-stu-id="c78d3-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="c78d3-124">La ligne suivante, tapée dans une fenêtre d’invite de commandes dans le même dossier que MsHDSP.dll, inscrit l’exemple de fournisseur de services :</span><span class="sxs-lookup"><span data-stu-id="c78d3-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="c78d3-125">Pour arrêter l’emprunt d’identité d’un appareil, entrez la ligne suivante à l’invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="c78d3-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="c78d3-126">Les appareils amovibles empruntés par cette DLL peuvent uniquement être vus par l’exemple d’application fourni avec ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c78d3-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="c78d3-127">Compilez l’exemple d’application à l’aide de l’une des méthodes décrites dans [exemple d’application de bureau](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="c78d3-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="c78d3-128">Pour déboguer le fournisseur de services avec Visual Studio, ouvrez le fournisseur de services dans Visual Studio et sélectionnez **Démarrer** dans le menu **Déboguer** .</span><span class="sxs-lookup"><span data-stu-id="c78d3-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="c78d3-129">Dans la boîte de dialogue contextuelle, accédez à l’exemple d’application que vous avez créé à l’étape précédente, puis cliquez sur **OK**. le fournisseur de services commence alors à s’exécuter en mode débogage.</span><span class="sxs-lookup"><span data-stu-id="c78d3-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="c78d3-130">Pour exécuter le fournisseur de services sans débogage dans Visual Studio, il vous suffit d’inscrire le msdhsp.dll et d’exécuter l’exemple d’application de bureau fourni avec le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="c78d3-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="c78d3-131">L’exemple d’application de bureau exécute automatiquement l’exemple de fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="c78d3-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c78d3-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c78d3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c78d3-133">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="c78d3-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




