---
title: Compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK)
description: Compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK)
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Gestionnaire de périphériques, fichiers IDL
- Gestionnaire de périphériques, fichiers IDL
- applications de bureau, fichiers IDL
- fournisseurs de services, fichiers IDL
- Guide de programmation, fichiers IDL
- fichiers IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444010"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a><span data-ttu-id="278ba-109">Compilation des fichiers IDL fournis avec le kit de développement logiciel (SDK)</span><span class="sxs-lookup"><span data-stu-id="278ba-109">Compiling the IDL Files Supplied with the SDK</span></span>

<span data-ttu-id="278ba-110">Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques comprend les fichiers d’en-tête et les fichiers IDL source pour la plupart de ces fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="278ba-110">The Windows Media Device Manager SDK includes both header files and the source IDL files for most of these header files.</span></span> <span data-ttu-id="278ba-111">Les fichiers d’en-tête se trouvent dans le \\ \\ dossier Inc dans le chemin d’installation du kit de développement logiciel.</span><span class="sxs-lookup"><span data-stu-id="278ba-111">The header files are located in the \\inc\\ folder in the SDK installation path.</span></span> <span data-ttu-id="278ba-112">Les fichiers IDL se trouvent dans le \\ \\ dossier IDL.</span><span class="sxs-lookup"><span data-stu-id="278ba-112">The IDL files are located in the \\idl\\ folder.</span></span>

<span data-ttu-id="278ba-113">Les en-têtes précompilés sont bien plus simples à utiliser, et plusieurs fichiers IDL sont combinés en un seul en-tête fourni.</span><span class="sxs-lookup"><span data-stu-id="278ba-113">The precompiled headers are much simpler to use, and several of the IDL files are combined into a single provided header.</span></span> <span data-ttu-id="278ba-114">Toutefois, si vous décidez de traiter vos propres fichiers d’en-tête à partir des fichiers IDL fournis, cette rubrique décrit les fichiers IDL qui créent les fichiers d’en-tête et décrit également les dépendances de chaque fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="278ba-114">However, if you decide to process your own header files from the provided IDL files, this topic describes which IDL files create which header files, and also describes the dependencies of each IDL file.</span></span>

<span data-ttu-id="278ba-115">**IDL équivalent et fichiers d’en-tête fournis**</span><span class="sxs-lookup"><span data-stu-id="278ba-115">**Equivalent IDL and Provided Header Files**</span></span>



| <span data-ttu-id="278ba-116">**MIDL**</span><span class="sxs-lookup"><span data-stu-id="278ba-116">**IDL**</span></span>                                                                                            | <span data-ttu-id="278ba-117">**En-tête fourni équivalent**</span><span class="sxs-lookup"><span data-stu-id="278ba-117">**Equivalent supplied header**</span></span>               | <span data-ttu-id="278ba-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="278ba-118">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="278ba-119">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-119">WMDM.idl</span></span><br/> <span data-ttu-id="278ba-120">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-120">WMSP.idl</span></span><br/> <span data-ttu-id="278ba-121">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-121">WMSCP.idl</span></span><br/> <span data-ttu-id="278ba-122">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-122">icomponentauthenticate.idl</span></span><br/> | <span data-ttu-id="278ba-123">Mswmdm. h</span><span class="sxs-lookup"><span data-stu-id="278ba-123">Mswmdm.h</span></span>                                     | <span data-ttu-id="278ba-124">Les quatre fichiers IDL sont inclus dans cet en-tête fourni unique.</span><span class="sxs-lookup"><span data-stu-id="278ba-124">All four IDL files are included in this single provided header.</span></span><br/> <span data-ttu-id="278ba-125">**WMDM. idl** définit toutes les interfaces d’application et les structures, les constantes et les codes d’erreur requis.</span><span class="sxs-lookup"><span data-stu-id="278ba-125">**WMDM.idl** Defines all the application interfaces and required structures, constants, and error codes.</span></span><br/> <span data-ttu-id="278ba-126">**Wmsp. idl** définit toutes les interfaces du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="278ba-126">**WMSP.idl** Defines all the service provider interfaces.</span></span><br/> <span data-ttu-id="278ba-127">**WMSCP. idl** définit toutes les interfaces, les valeurs GUID et les constantes requises par les fournisseurs de contenu sécurisé.</span><span class="sxs-lookup"><span data-stu-id="278ba-127">**WMSCP.idl** Defines all the interfaces, GUID values, and constants required by secure content providers.</span></span><br/> <span data-ttu-id="278ba-128">**icomponentauthenticate. idl** définit l’interface [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="278ba-128">**icomponentauthenticate.idl** Defines the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span><br/> |
| <span data-ttu-id="278ba-129">Wmdmlog. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-129">Wmdmlog.idl</span></span>                                                                                        | <span data-ttu-id="278ba-130">Wmdmlog. h</span><span class="sxs-lookup"><span data-stu-id="278ba-130">Wmdmlog.h</span></span><br/> <span data-ttu-id="278ba-131">wmdmlog \_ i. c</span><span class="sxs-lookup"><span data-stu-id="278ba-131">wmdmlog\_i.c</span></span><br/> | <span data-ttu-id="278ba-132">Définit les interfaces de journalisation.</span><span class="sxs-lookup"><span data-stu-id="278ba-132">Defines the logging interfaces.</span></span><br/> <span data-ttu-id="278ba-133">Les deux fichiers d’en-tête fournis doivent être utilisés, plutôt que simplement le fichier. h, en raison d’un problème avec le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="278ba-133">Both supplied header files must be used, rather than just the .h file, because of a problem with the IDL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="278ba-134">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-134">WMDRMDeviceApp.idl</span></span>                                                                                 | <span data-ttu-id="278ba-135">Wmdrmdeviceapp. h</span><span class="sxs-lookup"><span data-stu-id="278ba-135">Wmdrmdeviceapp.h</span></span>                             | <span data-ttu-id="278ba-136">Définit les interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) et [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) utilisées par les applications qui mettent à jour la DRM sur les appareils ou le nombre de jeux de lecture sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="278ba-136">Defines the [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) and [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) interfaces used by applications that update DRM on devices or meter play counts on devices.</span></span>                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="278ba-137">**Dépendances IDL**</span><span class="sxs-lookup"><span data-stu-id="278ba-137">**IDL Dependencies**</span></span>

<span data-ttu-id="278ba-138">Plusieurs des fichiers IDL fournis ont des dépendances de Build.</span><span class="sxs-lookup"><span data-stu-id="278ba-138">Several of the provided IDL files have build dependencies.</span></span> <span data-ttu-id="278ba-139">Si vous envisagez de compiler les fichiers IDL vous-même, vous devez traiter ces dépendances externes dans l’ordre indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="278ba-139">If you plan to compile the IDL files yourself, you must process these external dependencies in the order shown in the following table.</span></span>



|   <span data-ttu-id="278ba-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="278ba-140">IDL</span></span>                      |   <span data-ttu-id="278ba-141">Dépendances</span><span class="sxs-lookup"><span data-stu-id="278ba-141">Dependencies</span></span>                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="278ba-142">icomponentauthenticate. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-142">icomponentauthenticate.idl</span></span> | <span data-ttu-id="278ba-143">Importez « oaidl. idl »;</span><span class="sxs-lookup"><span data-stu-id="278ba-143">import "oaidl.idl";</span></span><br/> <span data-ttu-id="278ba-144">\#inclure « icomponentauthenticate. idl »</span><span class="sxs-lookup"><span data-stu-id="278ba-144">\#include "icomponentauthenticate.idl"</span></span><br/> |
| <span data-ttu-id="278ba-145">WMDM. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-145">WMDM.idl</span></span>                   | <span data-ttu-id="278ba-146">Aucune dépendance externe</span><span class="sxs-lookup"><span data-stu-id="278ba-146">No external dependencies</span></span>                                                         |
| <span data-ttu-id="278ba-147">WmdmLog. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-147">WmdmLog.idl</span></span>                | <span data-ttu-id="278ba-148">Aucune dépendance externe</span><span class="sxs-lookup"><span data-stu-id="278ba-148">No external dependencies</span></span>                                                         |
| <span data-ttu-id="278ba-149">WMDRMDeviceApp. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-149">WMDRMDeviceApp.idl</span></span>         | <span data-ttu-id="278ba-150">Aucune dépendance externe</span><span class="sxs-lookup"><span data-stu-id="278ba-150">No external dependencies</span></span>                                                         |
| <span data-ttu-id="278ba-151">WMSCP. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-151">WMSCP.idl</span></span>                  | <span data-ttu-id="278ba-152">\#inclure « WMDRMDeviceApp. idl »</span><span class="sxs-lookup"><span data-stu-id="278ba-152">\#include "WMDRMDeviceApp.idl"</span></span><br/> <span data-ttu-id="278ba-153">\#inclure « WMSP. idl »</span><span class="sxs-lookup"><span data-stu-id="278ba-153">\#include "WMSP.idl"</span></span><br/>        |
| <span data-ttu-id="278ba-154">WMSP. idl</span><span class="sxs-lookup"><span data-stu-id="278ba-154">WMSP.idl</span></span>                   | <span data-ttu-id="278ba-155">\#inclure « WMDM. idl »</span><span class="sxs-lookup"><span data-stu-id="278ba-155">\#include "WMDM.idl"</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="278ba-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="278ba-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="278ba-157">**Tâches communes aux applications et aux fournisseurs de services**</span><span class="sxs-lookup"><span data-stu-id="278ba-157">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





