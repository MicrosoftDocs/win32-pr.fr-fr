---
title: Constantes de package (AppModel. h)
description: Spécifie la manière dont les packages doivent être traités.
ms.assetid: 72E565C3-6CFD-47E3-8BAC-17D6E86B99DA
topic_type:
- apiref
api_name:
- PACKAGE_APPLICATIONS_MAX_COUNT
- PACKAGE_APPLICATIONS_MIN_COUNT
- PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES
- PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES
- PACKAGE_FILTER_ALL_LOADED
- PACKAGE_FILTER_BUNDLE
- PACKAGE_FILTER_DIRECT
- PACKAGE_FILTER_HEAD
- PACKAGE_FILTER_OPTIONAL
- PACKAGE_FILTER_RESOURCE
- PACKAGE_GRAPH_MAX_SIZE
- PACKAGE_GRAPH_MIN_SIZE
- PACKAGE_INFORMATION_BASIC
- PACKAGE_INFORMATION_FULL
- PACKAGE_MAX_DEPENDENCIES
- PACKAGE_MIN_DEPENDENCIES
- PACKAGE_PROPERTY_BUNDLE
- PACKAGE_PROPERTY_DEVELOPMENT_MODE
- PACKAGE_PROPERTY_FRAMEWORK
- PACKAGE_PROPERTY_OPTIONAL
- PACKAGE_PROPERTY_RESOURCE
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb3a4630eb6e132c7a82ea6b45839f6d2684cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510126"
---
# <a name="package-constants"></a><span data-ttu-id="64ea6-103">Constantes de package</span><span class="sxs-lookup"><span data-stu-id="64ea6-103">Package constants</span></span>

<span data-ttu-id="64ea6-104">Spécifie la manière dont les packages doivent être traités.</span><span class="sxs-lookup"><span data-stu-id="64ea6-104">Specifies how packages are to be processed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="64ea6-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="64ea6-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="64ea6-106">Description</span><span class="sxs-lookup"><span data-stu-id="64ea6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MAX_COUNT"></span><span id="package_applications_max_count"></span><dl> <span data-ttu-id="64ea6-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-107"><dt><strong>PACKAGE_APPLICATIONS_MAX_COUNT</strong></dt> <dt>100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-108">Nombre maximal d’applications dans un package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-108">The maximum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_APPLICATIONS_MIN_COUNT"></span><span id="package_applications_min_count"></span><dl> <span data-ttu-id="64ea6-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-109"><dt><strong>PACKAGE_APPLICATIONS_MIN_COUNT</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-110">Nombre minimal d’applications dans un package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-110">The minimum number of apps in a package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES"></span><span id="package_family_max_resource_packages"></span><dl> <span data-ttu-id="64ea6-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-111"><dt><strong>PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES</strong></dt> <dt>512</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-112">Nombre maximal de packages de ressources qu’un package peut avoir.</span><span class="sxs-lookup"><span data-stu-id="64ea6-112">The maximum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES"></span><span id="package_family_min_resource_packages"></span><dl> <span data-ttu-id="64ea6-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-113"><dt><strong>PACKAGE_FAMILY_MIN_RESOURCE_PACKAGES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-114">Nombre minimal de packages de ressources qu’un package peut avoir.</span><span class="sxs-lookup"><span data-stu-id="64ea6-114">The minimum number of resource packages a package can have.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_ALL_LOADED"></span><span id="package_filter_all_loaded"></span><dl> <span data-ttu-id="64ea6-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-115"><dt><strong>PACKAGE_FILTER_ALL_LOADED</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-116">Traiter tous les packages dans le graphique de dépendance.</span><span class="sxs-lookup"><span data-stu-id="64ea6-116">Process all packages in the dependency graph.</span></span><br/> <span data-ttu-id="64ea6-117">Cela équivaut à <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.</span><span class="sxs-lookup"><span data-stu-id="64ea6-117">This is equivalent to <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span><br/>
<blockquote>
[!Note]<br /><span data-ttu-id="64ea6-118">Les 
<strong>PACKAGE_FILTER_ALL_LOADED</strong> peuvent être modifiées ou indisponibles pour les mises en production après Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="64ea6-118">
<strong>PACKAGE_FILTER_ALL_LOADED</strong> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="64ea6-119">Au lieu de cela, utilisez <strong>PACKAGE_FILTER_HEAD</strong>  |  <strong>PACKAGE_FILTER_DIRECT</strong>.</span><span class="sxs-lookup"><span data-stu-id="64ea6-119">Instead, use <strong>PACKAGE_FILTER_HEAD</strong> | <strong>PACKAGE_FILTER_DIRECT</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_BUNDLE"></span><span id="package_filter_bundle"></span><dl> <span data-ttu-id="64ea6-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-120"><dt><strong>PACKAGE_FILTER_BUNDLE</strong></dt> <dt>0x00000080</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-121">Traiter les packages dans le graphique du package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-121">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_DIRECT"></span><span id="package_filter_direct"></span><dl> <span data-ttu-id="64ea6-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-122"><dt><strong>PACKAGE_FILTER_DIRECT</strong></dt> <dt>0x00000020</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-123">Traitez les packages directement dépendants du package Head (First) dans le graphique de dépendance.</span><span class="sxs-lookup"><span data-stu-id="64ea6-123">Process the directly dependent packages of the head (first) package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_HEAD"></span><span id="package_filter_head"></span><dl> <span data-ttu-id="64ea6-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-124"><dt><strong>PACKAGE_FILTER_HEAD</strong></dt> <dt>0x00000010</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-125">Traitez le premier package dans le graphique de dépendance.</span><span class="sxs-lookup"><span data-stu-id="64ea6-125">Process the first package in the dependency graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_FILTER_OPTIONAL"></span><span id="package_filter_optional"></span><dl> <span data-ttu-id="64ea6-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-126"><dt><strong>PACKAGE_FILTER_OPTIONAL</strong></dt> <dt>0x00020000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-127">Traiter les packages dans le graphique du package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-127">Process bundle packages in the package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_FILTER_RESOURCE"></span><span id="package_filter_resource"></span><dl> <span data-ttu-id="64ea6-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-128"><dt><strong>PACKAGE_FILTER_RESOURCE</strong></dt> <dt>0x00000040</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-129">Traitez les packages de ressources dans le graphique du package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-129">Process resource packages in the package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MAX_SIZE"></span><span id="package_graph_max_size"></span><dl> <span data-ttu-id="64ea6-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-130"><dt><strong>PACKAGE_GRAPH_MAX_SIZE</strong></dt> <dt>(1 + PACKAGE_MAX_DEPENDENCIES + PACKAGE_FAMILY_MAX_RESOURCE_PACKAGES)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-131">Taille maximale d’un graphique de package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-131">The maximum size of a package graph.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_GRAPH_MIN_SIZE"></span><span id="package_graph_min_size"></span><dl> <span data-ttu-id="64ea6-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-132"><dt><strong>PACKAGE_GRAPH_MIN_SIZE</strong></dt> <dt>1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-133">Taille minimale d’un graphique de package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-133">The minimum size of a package graph.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_BASIC"></span><span id="package_information_basic"></span><dl> <span data-ttu-id="64ea6-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-134"><dt><strong>PACKAGE_INFORMATION_BASIC</strong></dt> <dt>0x00000000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-135">Récupérer les informations de base.</span><span class="sxs-lookup"><span data-stu-id="64ea6-135">Retrieve basic information.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_INFORMATION_FULL"></span><span id="package_information_full"></span><dl> <span data-ttu-id="64ea6-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-136"><dt><strong>PACKAGE_INFORMATION_FULL</strong></dt> <dt>0x00000100</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-137">Récupérez des informations complètes.</span><span class="sxs-lookup"><span data-stu-id="64ea6-137">Retrieve full information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_MAX_DEPENDENCIES"></span><span id="package_max_dependencies"></span><dl> <span data-ttu-id="64ea6-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-138"><dt><strong>PACKAGE_MAX_DEPENDENCIES</strong></dt> <dt>128</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-139">Nombre maximal de packages dont dépend un package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-139">The maximum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_MIN_DEPENDENCIES"></span><span id="package_min_dependencies"></span><dl> <span data-ttu-id="64ea6-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-140"><dt><strong>PACKAGE_MIN_DEPENDENCIES</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-141">Nombre minimal de packages dont dépend un package.</span><span class="sxs-lookup"><span data-stu-id="64ea6-141">The minimum number of packages a package depends on.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_BUNDLE"></span><span id="package_property_bundle"></span><dl> <span data-ttu-id="64ea6-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-142"><dt><strong>PACKAGE_PROPERTY_BUNDLE</strong></dt> <dt>0x00000004</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-143">Le package est un package de bundle.</span><span class="sxs-lookup"><span data-stu-id="64ea6-143">The package is a bundle package.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_DEVELOPMENT_MODE"></span><span id="package_property_development_mode"></span><dl> <span data-ttu-id="64ea6-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-144"><dt><strong>PACKAGE_PROPERTY_DEVELOPMENT_MODE</strong></dt> <dt>0x00010000</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-145">Le package a été inscrit avec l’énumération <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>DeploymentOptions</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="64ea6-145">The package was registered with the <a href="/uwp/api/Windows.Management.Deployment.DeploymentOptions"><strong>DeploymentOptions</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_FRAMEWORK"></span><span id="package_property_framework"></span><dl> <span data-ttu-id="64ea6-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-146"><dt><strong>PACKAGE_PROPERTY_FRAMEWORK</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-147">Le package est un Framework.</span><span class="sxs-lookup"><span data-stu-id="64ea6-147">The package is a framework.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_OPTIONAL"></span><span id="package_property_optional"></span><dl> <span data-ttu-id="64ea6-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-148"><dt><strong>PACKAGE_PROPERTY_OPTIONAL</strong></dt> <dt>0x00000008</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-149">Le package est un package facultatif.</span><span class="sxs-lookup"><span data-stu-id="64ea6-149">The package is an optional package.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PACKAGE_PROPERTY_RESOURCE"></span><span id="package_property_resource"></span><dl> <span data-ttu-id="64ea6-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span><span class="sxs-lookup"><span data-stu-id="64ea6-150"><dt><strong>PACKAGE_PROPERTY_RESOURCE</strong></dt> <dt>0x00000002</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="64ea6-151">Le package est un package de ressources.</span><span class="sxs-lookup"><span data-stu-id="64ea6-151">The package is a resource package.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="64ea6-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64ea6-152">Requirements</span></span>



| <span data-ttu-id="64ea6-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64ea6-153">Requirement</span></span> | <span data-ttu-id="64ea6-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="64ea6-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64ea6-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64ea6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="64ea6-156">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64ea6-156">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="64ea6-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64ea6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="64ea6-158">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64ea6-158">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64ea6-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="64ea6-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="64ea6-160"><dt>AppModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="64ea6-160"><dt>AppModel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ea6-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64ea6-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ea6-162">**GetCurrentPackageInfo**</span><span class="sxs-lookup"><span data-stu-id="64ea6-162">**GetCurrentPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)
</dt> <dt>

[<span data-ttu-id="64ea6-163">**GetPackageInfo**</span><span class="sxs-lookup"><span data-stu-id="64ea6-163">**GetPackageInfo**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)
</dt> <dt>

[<span data-ttu-id="64ea6-164">**PackageIdFromFullName**</span><span class="sxs-lookup"><span data-stu-id="64ea6-164">**PackageIdFromFullName**</span></span>](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)
</dt> </dl>

 

