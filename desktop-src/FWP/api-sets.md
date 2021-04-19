---
title: API WFP
description: L’API WFP (Windows Filtering Platform) est composée des composants suivants.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "106509891"
---
# <a name="wfp-api"></a><span data-ttu-id="f77c8-103">API WFP</span><span class="sxs-lookup"><span data-stu-id="f77c8-103">WFP API</span></span>

<span data-ttu-id="f77c8-104">L’API WFP (Windows Filtering Platform) est composée des composants suivants.</span><span class="sxs-lookup"><span data-stu-id="f77c8-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f77c8-105">Composant</span><span class="sxs-lookup"><span data-stu-id="f77c8-105">Component</span></span></th>
<th><span data-ttu-id="f77c8-106">Description</span><span class="sxs-lookup"><span data-stu-id="f77c8-106">Description</span></span></th>
<th><span data-ttu-id="f77c8-107">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f77c8-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f77c8-108"><a href="/windows-hardware/drivers/ddi/_netvista/">API de légende</a> (FWPS) $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="f77c8-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f77c8-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Types de données</a> utilisés par les légendes. <strong>Remarque</strong>  Ces types de données sont documentés dans le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f77c8-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="f77c8-110">fwpstypes. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-110">fwpstypes.h</span></span><br />
<span data-ttu-id="f77c8-111">fwpstypes. idl</span><span class="sxs-lookup"><span data-stu-id="f77c8-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f77c8-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Fonctions</a> et <a href="/windows-hardware/drivers/ddi/_netvista/">types énumérés</a> utilisés pour implémenter des légendes. <strong>Remarque</strong>  Ces fonctions et types énumérés sont documentés dans le DDK.</span><span class="sxs-lookup"><span data-stu-id="f77c8-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="f77c8-113">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-113">fwpsu.h</span></span><br />
<span data-ttu-id="f77c8-114">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f77c8-115">API IKE/AuthIP (IKEEXT) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f77c8-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f77c8-116"><a href="fwp-enums.md">Types énumérés</a> et <a href="fwp-structs.md">structures</a> utilisés pour gérer les associations de sécurité et de stratégie en mode principal IKE et AuthIP.</span><span class="sxs-lookup"><span data-stu-id="f77c8-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f77c8-117">iketypes. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-117">iketypes.h</span></span><br />
<span data-ttu-id="f77c8-118">iketypes. idl</span><span class="sxs-lookup"><span data-stu-id="f77c8-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f77c8-119"><a href="fwp-ike-functions.md">Fonctions</a> utilisées pour gérer les associations de sécurité et de stratégie IKE et AuthIP mm.</span><span class="sxs-lookup"><span data-stu-id="f77c8-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f77c8-120">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-120">fwpmu.h</span></span><br />
<span data-ttu-id="f77c8-121">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f77c8-122">API IPsec (IPSEC) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f77c8-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f77c8-123"><a href="fwp-enums.md">Types</a> et <a href="fwp-structs.md">structures</a> énumérés utilisés pour la gestion des stratégies IPSec et des associations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f77c8-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f77c8-124">ipsectypes. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-124">ipsectypes.h</span></span><br />
<span data-ttu-id="f77c8-125">ipsectypes. idl</span><span class="sxs-lookup"><span data-stu-id="f77c8-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f77c8-126"><a href="fwp-ipsec-functions.md">Fonctions</a> utilisées pour gérer les stratégies IPSec et les associations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f77c8-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="f77c8-127">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-127">fwpmu.h</span></span><br />
<span data-ttu-id="f77c8-128">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="f77c8-129">API de gestion (FWPM) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="f77c8-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="f77c8-130"><a href="fwp-enums.md">Types</a> et <a href="fwp-structs.md">structures</a> énumérés utilisés pour la gestion du moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="f77c8-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="f77c8-131">fwpmtypes. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="f77c8-132">fwpmtypes. idl</span><span class="sxs-lookup"><span data-stu-id="f77c8-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f77c8-133"><a href="fwp-mgmt-functions.md">Fonctions</a> utilisées pour gérer le moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="f77c8-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="f77c8-134">Ces fonctions sont utilisées pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="f77c8-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="f77c8-135">Définir et interroger des filtres, des fournisseurs et des légendes.</span><span class="sxs-lookup"><span data-stu-id="f77c8-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="f77c8-136">Récupérez les statistiques IPsec.</span><span class="sxs-lookup"><span data-stu-id="f77c8-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="f77c8-137">Configurez la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="f77c8-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="f77c8-138">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-138">fwpmu.h</span></span><br />
<span data-ttu-id="f77c8-139">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="f77c8-140">API partagée (FWP)</span><span class="sxs-lookup"><span data-stu-id="f77c8-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="f77c8-141"><a href="fwp-structs.md">Structures</a> et <a href="fwp-enums.md">types énumérés</a> fondamentaux partagés sur la plateforme de filtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="f77c8-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="f77c8-142">fwptypes. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-142">fwptypes.h</span></span><br />
<span data-ttu-id="f77c8-143">fwptypes. idl</span><span class="sxs-lookup"><span data-stu-id="f77c8-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f77c8-144">Les noms des types de données sont tous des majuscules et des traits de soulignement, délimités.</span><span class="sxs-lookup"><span data-stu-id="f77c8-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="f77c8-145">Le nom commence toujours par un préfixe qui identifie son groupe de composants, par exemple [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span><span class="sxs-lookup"><span data-stu-id="f77c8-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="f77c8-146">Les noms de fonction sont en casse mixte et délimités par la casse.</span><span class="sxs-lookup"><span data-stu-id="f77c8-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="f77c8-147">Le nom commence toujours par un préfixe qui identifie son groupe de composants, par exemple [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span><span class="sxs-lookup"><span data-stu-id="f77c8-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="f77c8-148">La plupart des noms de données et de fonctions se terminent par un numéro de version.</span><span class="sxs-lookup"><span data-stu-id="f77c8-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="f77c8-149">Le fichier d’en-tête fwpvi. h mappe des données et des noms de fonction indépendants de la version à la version qui est appropriée pour une utilisation avec un système d’exploitation donné.</span><span class="sxs-lookup"><span data-stu-id="f77c8-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="f77c8-150">Pour plus d’informations, consultez [noms de Version-Independent WFP et cibler des versions spécifiques de Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="f77c8-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="f77c8-151">Chaque composant n’est pas autonome.</span><span class="sxs-lookup"><span data-stu-id="f77c8-151">Each component does not stand alone.</span></span> <span data-ttu-id="f77c8-152">Par exemple, les stratégies en mode principal IKE (MM) sont définies dans le composant IKEEXT, mais elles sont stockées dans un contexte de fournisseur et sont associées à un filtre qui se trouve dans le composant de l’API FWPM.</span><span class="sxs-lookup"><span data-stu-id="f77c8-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="f77c8-153">Fichiers d’en-tête publics User-Mode et Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="f77c8-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="f77c8-154">La plupart des fonctions WFP peuvent être appelées à partir du mode utilisateur ou du mode noyau.</span><span class="sxs-lookup"><span data-stu-id="f77c8-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="f77c8-155">Toutefois, les fonctions en mode utilisateur retournent une valeur **DWORD** qui représente un code d’erreur Win32, tandis que les fonctions en mode noyau retournent une valeur **NTSTATUS** qui représente un code d’état NT.</span><span class="sxs-lookup"><span data-stu-id="f77c8-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="f77c8-156">Par conséquent, les noms de fonction et la sémantique sont identiques entre le mode utilisateur et le mode noyau, mais pas les signatures de fonction.</span><span class="sxs-lookup"><span data-stu-id="f77c8-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="f77c8-157">Cela requiert des en-têtes spécifiques en mode utilisateur et en mode noyau pour les prototypes de fonction.</span><span class="sxs-lookup"><span data-stu-id="f77c8-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="f77c8-158">Les noms de fichiers d’en-tête en mode utilisateur se terminent par « u » et les noms de fichiers d’en-tête en mode noyau se terminent par « k ».</span><span class="sxs-lookup"><span data-stu-id="f77c8-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="f77c8-159">Le tableau suivant répertorie les fichiers d’en-tête Win32 qui définissent les fonctions WFP.</span><span class="sxs-lookup"><span data-stu-id="f77c8-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="f77c8-160">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f77c8-160">Header Files</span></span> | <span data-ttu-id="f77c8-161">Description</span><span class="sxs-lookup"><span data-stu-id="f77c8-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f77c8-162">fwpmk. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-162">fwpmk.h</span></span>      | <span data-ttu-id="f77c8-163">Prototypes de fonction en mode noyau pour les composants FWPM, IPsec et IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="f77c8-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="f77c8-164">Disponible uniquement dans le DDK.</span><span class="sxs-lookup"><span data-stu-id="f77c8-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f77c8-165">fwpmu. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-165">fwpmu.h</span></span>      | <span data-ttu-id="f77c8-166">Prototypes de fonction en mode utilisateur pour les composants FWPM, IPsec et IKEEXT.</span><span class="sxs-lookup"><span data-stu-id="f77c8-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="f77c8-167">Disponible uniquement dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f77c8-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f77c8-168">fwpsk. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-168">fwpsk.h</span></span>      | <span data-ttu-id="f77c8-169">Prototypes de fonction en mode noyau et types énumérés pour le composant FWPS.</span><span class="sxs-lookup"><span data-stu-id="f77c8-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="f77c8-170">Disponible uniquement dans le DDK.</span><span class="sxs-lookup"><span data-stu-id="f77c8-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f77c8-171">fwpsu. h</span><span class="sxs-lookup"><span data-stu-id="f77c8-171">fwpsu.h</span></span>      | <span data-ttu-id="f77c8-172">Prototypes de fonction en mode utilisateur et types énumérés pour le composant FWPS.</span><span class="sxs-lookup"><span data-stu-id="f77c8-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="f77c8-173">Disponible dans le SDK Windows uniquement. **Remarque**  Les types énumérés FWPS en mode utilisateur sont identiques aux types énumérés FWPS en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="f77c8-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="f77c8-174">En conséquence, ces types sont documentés uniquement dans le DDK.</span><span class="sxs-lookup"><span data-stu-id="f77c8-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="f77c8-175">**Remarque**  Les prototypes de fonction FWPS en mode utilisateur sont identiques aux prototypes de fonction FWPS en mode noyau, à l’exception du code de retour.</span><span class="sxs-lookup"><span data-stu-id="f77c8-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="f77c8-176">Les fonctions FWPS en mode utilisateur retournent une **valeur DWORD**, tandis que les fonctions FWPS en mode noyau retournent un **NTSTATUS**.</span><span class="sxs-lookup"><span data-stu-id="f77c8-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="f77c8-177">En conséquence, ces fonctions sont documentées dans le DDK uniquement.</span><span class="sxs-lookup"><span data-stu-id="f77c8-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="f77c8-178">Toutes les fonctions en mode utilisateur sont exportées à partir de fwpuclnt.dll.</span><span class="sxs-lookup"><span data-stu-id="f77c8-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="f77c8-179">Toutes les fonctions en mode noyau sont exportées à partir de fwpkclnt.sys.</span><span class="sxs-lookup"><span data-stu-id="f77c8-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="f77c8-180">Types de données Management (FWPM) et Callout (FWPS)</span><span class="sxs-lookup"><span data-stu-id="f77c8-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="f77c8-181">La plupart des types de données FWPM, qui sont utilisés pour les tâches de gestion telles que l’ajout de filtres ou de légendes à partir d’une application ou d’un pilote, ont des équivalents FWPS.</span><span class="sxs-lookup"><span data-stu-id="f77c8-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="f77c8-182">Les types de données FWPS sont utilisés lors du filtrage réel du trafic réseau, dans le contexte d’une routine de légende pour la classification.</span><span class="sxs-lookup"><span data-stu-id="f77c8-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="f77c8-183">Par exemple, pour ajouter un filtre à une certaine couche du moteur de filtrage, le programmeur doit utiliser un type FWPM, comme : `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` .</span><span class="sxs-lookup"><span data-stu-id="f77c8-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="f77c8-184">Pour vérifier la couche à partir de laquelle une légende est appelée, le programmeur doit utiliser le type FWPS correspondant : ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .</span><span class="sxs-lookup"><span data-stu-id="f77c8-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="f77c8-185">Certains FWPS équivalents aux types de données FWPM développent les types de données FWPM d’origine.</span><span class="sxs-lookup"><span data-stu-id="f77c8-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="f77c8-186">Par exemple, pour ajouter une condition de filtre à de nombreuses couches du moteur de filtrage, le programmeur spécifie `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` quelle que soit la couche du moteur de filtrage.</span><span class="sxs-lookup"><span data-stu-id="f77c8-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="f77c8-187">Pour rechercher une valeur de condition de filtre, le programmeur spécifie un type FWPS spécifique à la couche, par exemple : `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .</span><span class="sxs-lookup"><span data-stu-id="f77c8-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="f77c8-188">Les types de données FWPS sont généralement plus petits que leurs équivalents FWPM.</span><span class="sxs-lookup"><span data-stu-id="f77c8-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="f77c8-189">Par exemple, les [**identificateurs de couche de filtrage FWPM**](management-filtering-layer-identifiers-.md) sont des **GUID** s (16 octets) tandis que les [identificateurs de couche de filtrage FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) sont **UINT16** (16 bits).</span><span class="sxs-lookup"><span data-stu-id="f77c8-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="f77c8-190">La taille réduite pour les types de données FWPS améliore les performances du système, car les comparaisons de nombres entiers compensent les comparaisons de **GUID** pour le trafic en temps réel.</span><span class="sxs-lookup"><span data-stu-id="f77c8-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="f77c8-191">En outre, la mémoire du noyau est utilisée efficacement, car les types FWPS sont utilisés dans le noyau pour gérer les filtres, tandis que les types FWPM sont stockés en mode utilisateur pour gérer les différentes couches.</span><span class="sxs-lookup"><span data-stu-id="f77c8-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f77c8-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f77c8-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f77c8-193">Modèle objet de l’API WFP</span><span class="sxs-lookup"><span data-stu-id="f77c8-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="f77c8-194">Gestion des objets de l’API WFP</span><span class="sxs-lookup"><span data-stu-id="f77c8-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>

