---
description: Cette rubrique fournit des instructions pour l’installation ou la réinstallation d’une installation de plusieurs instances qui utilise des transformations d’instance.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installation de plusieurs instances à l’aide de transformations d’instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034143"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="66e7b-103">Installation de plusieurs instances à l’aide de transformations d’instance</span><span class="sxs-lookup"><span data-stu-id="66e7b-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="66e7b-104">Cette rubrique fournit des instructions pour l’installation ou la réinstallation d’une installation de plusieurs instances qui utilise des transformations d’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="66e7b-105">Lors de l’installation d’une nouvelle instance avec une transformation d’instance, incluez la propriété **MSINEWINSTANCE** et définissez **MSINEWINSTANCE**= 1.</span><span class="sxs-lookup"><span data-stu-id="66e7b-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="66e7b-106">Lors de l’installation d’une nouvelle instance de à l’aide d’une transformation d’instance, incluez la propriété transformations et définissez la première transformation de la liste des transformations sur la transformation d’instance qui modifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="66e7b-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="66e7b-107">Toutes les transformations de personnalisation doivent suivre la transformation d’instance au début de cette liste.</span><span class="sxs-lookup"><span data-stu-id="66e7b-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="66e7b-108">Le moyen le plus simple d’effectuer une installation de maintenance et de réinstaller une instance consiste à faire référence au code de produit de l’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="66e7b-109">Si vous lancez l’installation de maintenance à l’aide du chemin d’accès au package, vous devez également spécifier le code de produit de l’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="66e7b-110">À partir de la ligne de commande, utilisez l’option/n {Product Code}.</span><span class="sxs-lookup"><span data-stu-id="66e7b-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="66e7b-111">À partir du code ou du script, utilisez la propriété **MSIINSTANCEGUID** .</span><span class="sxs-lookup"><span data-stu-id="66e7b-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="66e7b-112">L’exemple suivant montre comment installer une nouvelle instance à partir d’une ligne de commande dans laquelle la transformation d’instance est précédée d’un signe deux-points qui spécifie que la transformation est incorporée dans le package.</span><span class="sxs-lookup"><span data-stu-id="66e7b-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="66e7b-113">**msiexec/I mypackage.msi transformations = : instance. MST MSINEWINSTANCE = 1/QB**</span><span class="sxs-lookup"><span data-stu-id="66e7b-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="66e7b-114">L’exemple suivant illustre l’installation d’une nouvelle instance de à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span><span class="sxs-lookup"><span data-stu-id="66e7b-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="66e7b-115">L’exemple suivant illustre l’installation de la nouvelle instance à partir d’un script.</span><span class="sxs-lookup"><span data-stu-id="66e7b-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="66e7b-116">L’exemple suivant réinstalle une instance sans remettre en cache le package.</span><span class="sxs-lookup"><span data-stu-id="66e7b-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="66e7b-117">L’instance est référencée par son code de produit {00000001-0002-0000-0000-624474736554} .</span><span class="sxs-lookup"><span data-stu-id="66e7b-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="66e7b-118">**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**</span><span class="sxs-lookup"><span data-stu-id="66e7b-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="66e7b-119">L’exemple suivant réinstalle une instance et met à nouveau le package à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="66e7b-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="66e7b-120">L’instance est référencée par le chemin d’accès au package.</span><span class="sxs-lookup"><span data-stu-id="66e7b-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="66e7b-121">Vous devez uniquement inclure l’option/n {Product Code} si le produit est installé à l’origine avec une transformation d’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="66e7b-122">**msiexec/I c : \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/QB**</span><span class="sxs-lookup"><span data-stu-id="66e7b-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="66e7b-123">L’exemple suivant réinstalle une instance de et met en cache le package à l’aide de **MsiInstallProduct**.</span><span class="sxs-lookup"><span data-stu-id="66e7b-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="66e7b-124">L’instance est référencée par le chemin d’accès au package.</span><span class="sxs-lookup"><span data-stu-id="66e7b-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="66e7b-125">Utilisez la propriété **MSIINSTANCEGUID** pour fournir le code de produit de l’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="66e7b-126">L’exemple suivant réinstalle une instance de et met en cache le package à l’aide d’un script.</span><span class="sxs-lookup"><span data-stu-id="66e7b-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="66e7b-127">Utilisez la propriété **MSIINSTANCEGUID** pour fournir le code de produit de l’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="66e7b-128">L’exemple suivant montre comment publier une instance à l’aide de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="66e7b-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="66e7b-129">**msiexec/JM mypackage.msi/t : instance. MST/c/QB**</span><span class="sxs-lookup"><span data-stu-id="66e7b-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="66e7b-130">L’exemple suivant montre comment installer pour publier une instance à l’aide de **MsiAdvertiseProductEx**.</span><span class="sxs-lookup"><span data-stu-id="66e7b-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="66e7b-131">L’exemple suivant montre comment appliquer un correctif à une instance à partir d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="66e7b-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="66e7b-132">Vous devez uniquement inclure l’option/n {Product Code} si le produit a été installé à l’origine avec une transformation d’instance.</span><span class="sxs-lookup"><span data-stu-id="66e7b-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="66e7b-133">**msiexec/p mypatch. msp/n {00000001-0002-0000-0000-624474736554} /qb**</span><span class="sxs-lookup"><span data-stu-id="66e7b-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="66e7b-134">L’exemple suivant montre comment appliquer un correctif à une installation d’instance à l’aide de [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span><span class="sxs-lookup"><span data-stu-id="66e7b-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="66e7b-135">Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md) et [création de plusieurs instances à l’aide de transformations d’instance](authoring-multiple-instances-with-instance-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="66e7b-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 



