---
description: La bibliothèque d’administration MTS fournie avec les interfaces d’administration COM+ offre une compatibilité descendante avec la bibliothèque d’administration MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Bibliothèque d’administration MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523540"
---
# <a name="mts-administration-library"></a><span data-ttu-id="5638c-103">Bibliothèque d’administration MTS</span><span class="sxs-lookup"><span data-stu-id="5638c-103">MTS Administration Library</span></span>

<span data-ttu-id="5638c-104">La bibliothèque d’administration MTS fournie avec les interfaces d’administration COM+ offre une compatibilité descendante avec la bibliothèque d’administration MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="5638c-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="5638c-105">La plupart des codes d’administration MTS 2,0 existants fonctionnent toujours avec la bibliothèque MTSAdmin fournie. Toutefois, certaines fonctionnalités ont changé.</span><span class="sxs-lookup"><span data-stu-id="5638c-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="5638c-106">Pour tirer parti de nouvelles fonctionnalités ou si vous écrivez du code d’administration pour la première fois, vous devez utiliser la bibliothèque comadmin.</span><span class="sxs-lookup"><span data-stu-id="5638c-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="5638c-107">Les éléments suivants de la bibliothèque d’administration MTS actuelle sont modifiés à partir de la bibliothèque d’administration MTS 2,0 :</span><span class="sxs-lookup"><span data-stu-id="5638c-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="5638c-108">L’interface **IRemoteComponentUtil** n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="5638c-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="5638c-109">La collection **RemoteComponents** n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="5638c-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="5638c-110">La propriété RoleID n’est plus disponible, le nom de rôle est maintenant utilisé comme clé pour ce.</span><span class="sxs-lookup"><span data-stu-id="5638c-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="5638c-111">La méthode **ExportPackage** n’exporte plus de client.exe.</span><span class="sxs-lookup"><span data-stu-id="5638c-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="5638c-112">La propriété RemoteComponentInstallPath n’est plus exposée sur la collection [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="5638c-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="5638c-113">La propriété ApplicationInstallPath ne sera plus exposée sur la collection [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="5638c-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="5638c-114">Le package système est maintenant nommé application système.</span><span class="sxs-lookup"><span data-stu-id="5638c-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="5638c-115">Le package Utilities est maintenant nommé utilitaires COM+.</span><span class="sxs-lookup"><span data-stu-id="5638c-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="5638c-116">La propriété IsSystem existe dans la collection de [**composants**](components.md) dans MTSAdmin, mais retourne « NotImpl » quand elle est activée et n’est pas enregistrée si elle est définie.</span><span class="sxs-lookup"><span data-stu-id="5638c-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="5638c-117">La propriété PackageName n’est plus prise en charge par la collection de [**composants**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="5638c-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="5638c-118">Pour déterminer le nom du package, vous devez maintenant obtenir le PackageID, puis rechercher le package correspondant dans la collection de packages.</span><span class="sxs-lookup"><span data-stu-id="5638c-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="5638c-119">Les propriétés suivantes n’existent plus sur la collection [**InterfacesForComponent**](interfacesforcomponent.md) :</span><span class="sxs-lookup"><span data-stu-id="5638c-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="5638c-120">**ProxyCLSID**</span><span class="sxs-lookup"><span data-stu-id="5638c-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="5638c-121">**ProxyDLL**</span><span class="sxs-lookup"><span data-stu-id="5638c-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="5638c-122">**ProxyThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="5638c-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="5638c-123">**TypeLibFile**</span><span class="sxs-lookup"><span data-stu-id="5638c-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="5638c-124">**TypeLibID**</span><span class="sxs-lookup"><span data-stu-id="5638c-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="5638c-125">**TypeLibLangID**</span><span class="sxs-lookup"><span data-stu-id="5638c-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="5638c-126">**TypeLibPlatform**</span><span class="sxs-lookup"><span data-stu-id="5638c-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="5638c-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="5638c-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="5638c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5638c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5638c-129">Conversion automatique à partir de MTS</span><span class="sxs-lookup"><span data-stu-id="5638c-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="5638c-130">Résultats et problèmes de conversion COM+</span><span class="sxs-lookup"><span data-stu-id="5638c-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="5638c-131">Conversion manuelle à partir de MTS</span><span class="sxs-lookup"><span data-stu-id="5638c-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



