---
title: Inscription des extensions de classe d’assistance NDF
description: Chaque extension de classe d’assistance est associée à un certain nombre de clés de registre. Certaines clés sont requises par COM, et certaines clés sont requises par NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675981"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="504f0-104">Inscription des extensions de classe d’assistance NDF</span><span class="sxs-lookup"><span data-stu-id="504f0-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="504f0-105">Chaque extension de classe d’assistance est associée à un certain nombre de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="504f0-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="504f0-106">Certaines clés sont requises par COM, et certaines clés sont requises par NDF.</span><span class="sxs-lookup"><span data-stu-id="504f0-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="504f0-107">Clés de registre COM</span><span class="sxs-lookup"><span data-stu-id="504f0-107">COM Registry Keys</span></span>

<span data-ttu-id="504f0-108">Les extensions de classe d’assistance doivent être implémentées en tant que serveurs COM.</span><span class="sxs-lookup"><span data-stu-id="504f0-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="504f0-109">L’inscription COM doit être effectuée pour chaque extension de la classe d’assistance.</span><span class="sxs-lookup"><span data-stu-id="504f0-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="504f0-110">Le CLSID de l’objet, l’interface [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) et l’interface [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) doivent être inscrits.</span><span class="sxs-lookup"><span data-stu-id="504f0-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="504f0-111">L’inscription crée un certain nombre de clés de Registre liées à COM pour l’extension de classe d’assistance NDF.</span><span class="sxs-lookup"><span data-stu-id="504f0-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="504f0-112">Clés de Registre NDF</span><span class="sxs-lookup"><span data-stu-id="504f0-112">NDF Registry Keys</span></span>

<span data-ttu-id="504f0-113">Les extensions de classe d’assistance doivent être inscrites avant l’interaction avec l’infrastructure de diagnostics réseau et avec d’autres classes d’assistance associées.</span><span class="sxs-lookup"><span data-stu-id="504f0-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="504f0-114">Pour ce faire, vous devez remplir le registre.</span><span class="sxs-lookup"><span data-stu-id="504f0-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="504f0-115">La procédure suivante montre comment ajouter des extensions de classe d’assistance au registre.</span><span class="sxs-lookup"><span data-stu-id="504f0-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="504f0-116">Publiez les noms des classes d’assistance implémentées par la DLL et leurs dépendances en créant une clé pour la DLL sous</span><span class="sxs-lookup"><span data-stu-id="504f0-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="504f0-117">**HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *NomFournisseur* \\ **HostDLLs** \\ *classe d’assistance dll* \\ **HelperClasses** \\ *nom de classe d’assistance*</span><span class="sxs-lookup"><span data-stu-id="504f0-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="504f0-118">Remplacez *NomFournisseur*, *dll de la classe d’assistance* et le nom de la *classe d’assistance* par des valeurs définies par l’utilisateur, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="504f0-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="504f0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="504f0-119">Value</span></span>               | <span data-ttu-id="504f0-120">Type</span><span class="sxs-lookup"><span data-stu-id="504f0-120">Type</span></span>    | <span data-ttu-id="504f0-121">Signification</span><span class="sxs-lookup"><span data-stu-id="504f0-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="504f0-122">*VendorName*</span><span class="sxs-lookup"><span data-stu-id="504f0-122">*VendorName*</span></span>        | <span data-ttu-id="504f0-123">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="504f0-123">REG\_SZ</span></span> | <span data-ttu-id="504f0-124">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="504f0-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="504f0-125">*DLL de la classe d’assistance*</span><span class="sxs-lookup"><span data-stu-id="504f0-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="504f0-126">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="504f0-126">REG\_SZ</span></span> | <span data-ttu-id="504f0-127">Nom de la DLL, sans extension.</span><span class="sxs-lookup"><span data-stu-id="504f0-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="504f0-128">*Nom de la classe d’assistance*</span><span class="sxs-lookup"><span data-stu-id="504f0-128">*Helper Class Name*</span></span> | <span data-ttu-id="504f0-129">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="504f0-129">REG\_SZ</span></span> | <span data-ttu-id="504f0-130">Nom de la classe d’assistance dont dépend la classe d’assistance actuelle.</span><span class="sxs-lookup"><span data-stu-id="504f0-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="504f0-131">Sous chaque clé de *nom de classe d’assistance* , publiez les informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="504f0-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="504f0-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="504f0-132">Value</span></span>         | <span data-ttu-id="504f0-133">Type</span><span class="sxs-lookup"><span data-stu-id="504f0-133">Type</span></span>       | <span data-ttu-id="504f0-134">Signification</span><span class="sxs-lookup"><span data-stu-id="504f0-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="504f0-135">**IDENTIFICATEUR**</span><span class="sxs-lookup"><span data-stu-id="504f0-135">**CLSID**</span></span>     | <span data-ttu-id="504f0-136">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="504f0-136">REG\_SZ</span></span>    | <span data-ttu-id="504f0-137">Chaîne qui contient l’ID de classe COM de la classe d’assistance.</span><span class="sxs-lookup"><span data-stu-id="504f0-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="504f0-138">**Version**</span><span class="sxs-lookup"><span data-stu-id="504f0-138">**Version**</span></span>   | <span data-ttu-id="504f0-139">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="504f0-139">REG\_SZ</span></span>    | <span data-ttu-id="504f0-140">Chaîne qui contient les versions principales et secondaires de la classe d’assistance dans le format <major> <minor> .</span><span class="sxs-lookup"><span data-stu-id="504f0-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="504f0-141">**Publié**</span><span class="sxs-lookup"><span data-stu-id="504f0-141">**Published**</span></span> | <span data-ttu-id="504f0-142">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="504f0-142">REG\_DWORD</span></span> | <span data-ttu-id="504f0-143">La valeur 1 signifie que cette classe d’assistance est supposée être appelée directement à partir du client de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="504f0-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="504f0-144">0 signifie qu’il ne peut être appelé qu’à partir d’une autre classe d’assistance.</span><span class="sxs-lookup"><span data-stu-id="504f0-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="504f0-145">**Parent**</span><span class="sxs-lookup"><span data-stu-id="504f0-145">**Parent**</span></span>    | <span data-ttu-id="504f0-146">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="504f0-146">REG\_SZ</span></span>    | <span data-ttu-id="504f0-147">Chaîne qui nomme la classe d’assistance extensible Microsoft qui est étendue.</span><span class="sxs-lookup"><span data-stu-id="504f0-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="504f0-148">Pour chaque classe d’assistance, publiez la liste des attributs correspondants en créant une clé sous</span><span class="sxs-lookup"><span data-stu-id="504f0-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="504f0-149">**HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *NomFournisseur* \\ **HostDLLs** \\ *classe d’assistance dll* \\ **HelperClasses** \\ *nom de classe d’assistance* \\ **MatchAttributes**</span><span class="sxs-lookup"><span data-stu-id="504f0-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="504f0-150">Elles doivent contenir une ou plusieurs valeurs (une par attribut) du type suivant.</span><span class="sxs-lookup"><span data-stu-id="504f0-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="504f0-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="504f0-151">Value</span></span>             | <span data-ttu-id="504f0-152">Type</span><span class="sxs-lookup"><span data-stu-id="504f0-152">Type</span></span>                             | <span data-ttu-id="504f0-153">Signification</span><span class="sxs-lookup"><span data-stu-id="504f0-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="504f0-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="504f0-154">**AttributeName**</span></span> | <span data-ttu-id="504f0-155">reg \_ SZ \| reg \_ \| \_ fichier binaire reg</span><span class="sxs-lookup"><span data-stu-id="504f0-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="504f0-156">Valeur qui complète la paire nom/valeur d’un attribut particulier.</span><span class="sxs-lookup"><span data-stu-id="504f0-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




