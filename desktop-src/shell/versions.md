---
description: Cette section décrit comment déterminer la version des dll Shell sur laquelle votre application s’exécute et comment cibler votre application pour une version spécifique.
title: Versions des DLL Shell et Shlwapi
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202768"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="8c34d-103">Versions des DLL Shell et Shlwapi</span><span class="sxs-lookup"><span data-stu-id="8c34d-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="8c34d-104">Cette section décrit comment déterminer la version des dll Shell sur laquelle votre application s’exécute et comment cibler votre application pour une version spécifique.</span><span class="sxs-lookup"><span data-stu-id="8c34d-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="8c34d-105">Numéros de version des DLL</span><span class="sxs-lookup"><span data-stu-id="8c34d-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="8c34d-106">Utilisation de DllGetVersion pour déterminer le numéro de version</span><span class="sxs-lookup"><span data-stu-id="8c34d-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="8c34d-107">Utilisation de DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="8c34d-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="8c34d-108">Versions du projet</span><span class="sxs-lookup"><span data-stu-id="8c34d-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="8c34d-109">Numéros de version des DLL</span><span class="sxs-lookup"><span data-stu-id="8c34d-109">DLL Version Numbers</span></span>

<span data-ttu-id="8c34d-110">Tous les éléments de programmation, à l’exception de quelques-uns, décrits dans la documentation de l’interpréteur de commandes sont contenus dans deux dll : Shell32.dll et Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="8c34d-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="8c34d-111">En raison des améliorations en cours, différentes versions de ces dll implémentent des fonctionnalités différentes.</span><span class="sxs-lookup"><span data-stu-id="8c34d-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="8c34d-112">Tout au long de la documentation de référence du shell, chaque élément de programmation spécifie un numéro de version DLL minimal pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8c34d-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="8c34d-113">Ce numéro de version indique que l’élément de programmation est implémenté dans cette version et les versions ultérieures de la DLL, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="8c34d-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="8c34d-114">Si aucun numéro de version n’est spécifié, l’élément de programmation est implémenté dans toutes les versions existantes de la DLL.</span><span class="sxs-lookup"><span data-stu-id="8c34d-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="8c34d-115">Avant Windows XP, les nouvelles versions de Shell32.dll et Shlwapi.dll étaient parfois fournies avec les nouvelles versions de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8c34d-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="8c34d-116">À compter de Windows XP, ces dll n’étaient plus fournies comme des fichiers redistribuables en dehors des nouvelles versions de Windows elle-même.</span><span class="sxs-lookup"><span data-stu-id="8c34d-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="8c34d-117">Le tableau suivant présente les différentes versions des DLL et la façon dont elles ont été distribuées à nouveau vers Microsoft Internet Explorer 3,0, Windows 95 et Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="8c34d-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="8c34d-118">Shell32.dll version 4,0 est disponible dans les versions d’origine de Windows 95 et Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="8c34d-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="8c34d-119">L’interpréteur de commandes n’a pas été mis à jour avec la version 3,0 d’Internet Explorer, donc Shell32.dll n’a pas de version 4,70.</span><span class="sxs-lookup"><span data-stu-id="8c34d-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="8c34d-120">Les versions 4,71 et 4,72 de Shell32.dll étaient fournies avec les versions d’Internet Explorer correspondantes, mais elles n’étaient pas nécessairement installées (voir la remarque 1).</span><span class="sxs-lookup"><span data-stu-id="8c34d-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="8c34d-121">Pour les versions ultérieures à Microsoft Internet Explorer 4,01 et Windows 98, les numéros de version pour Shell32.dll et Shlwapi.dll divergent.</span><span class="sxs-lookup"><span data-stu-id="8c34d-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="8c34d-122">En général, vous devez supposer que les dll ont des numéros de version différents et tester chacune d’elles séparément.</span><span class="sxs-lookup"><span data-stu-id="8c34d-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="8c34d-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="8c34d-123">Shell32.dll</span></span>

| <span data-ttu-id="8c34d-124">Version</span><span class="sxs-lookup"><span data-stu-id="8c34d-124">Version</span></span> | <span data-ttu-id="8c34d-125">Plateforme de distribution</span><span class="sxs-lookup"><span data-stu-id="8c34d-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8c34d-126">4.0</span><span class="sxs-lookup"><span data-stu-id="8c34d-126">4.0</span></span>     | <span data-ttu-id="8c34d-127">Windows 95 et Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="8c34d-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="8c34d-128">4.71</span><span class="sxs-lookup"><span data-stu-id="8c34d-128">4.71</span></span>    | <span data-ttu-id="8c34d-129">Microsoft Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="8c34d-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="8c34d-130">Consultez la remarque 1.</span><span class="sxs-lookup"><span data-stu-id="8c34d-130">See note 1.</span></span>                                |
| <span data-ttu-id="8c34d-131">4.72</span><span class="sxs-lookup"><span data-stu-id="8c34d-131">4.72</span></span>    | <span data-ttu-id="8c34d-132">Internet Explorer 4,01 et Windows 98.</span><span class="sxs-lookup"><span data-stu-id="8c34d-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="8c34d-133">Consultez la remarque 1.</span><span class="sxs-lookup"><span data-stu-id="8c34d-133">See note 1.</span></span>                          |
| <span data-ttu-id="8c34d-134">5.0</span><span class="sxs-lookup"><span data-stu-id="8c34d-134">5.0</span></span>     | <span data-ttu-id="8c34d-135">Windows 2000 et Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="8c34d-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="8c34d-136">Voir la remarque 2.</span><span class="sxs-lookup"><span data-stu-id="8c34d-136">See note 2.</span></span>       |
| <span data-ttu-id="8c34d-137">6.0</span><span class="sxs-lookup"><span data-stu-id="8c34d-137">6.0</span></span>     | <span data-ttu-id="8c34d-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c34d-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="8c34d-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="8c34d-139">6.0.1</span></span>   | <span data-ttu-id="8c34d-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c34d-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="8c34d-141">6.1</span><span class="sxs-lookup"><span data-stu-id="8c34d-141">6.1</span></span>     | <span data-ttu-id="8c34d-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c34d-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="8c34d-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="8c34d-143">Shlwapi.dll</span></span>

| <span data-ttu-id="8c34d-144">Version</span><span class="sxs-lookup"><span data-stu-id="8c34d-144">Version</span></span> | <span data-ttu-id="8c34d-145">Plateforme de distribution</span><span class="sxs-lookup"><span data-stu-id="8c34d-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8c34d-146">4.0</span><span class="sxs-lookup"><span data-stu-id="8c34d-146">4.0</span></span>     | <span data-ttu-id="8c34d-147">Windows 95 et Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="8c34d-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="8c34d-148">4.71</span><span class="sxs-lookup"><span data-stu-id="8c34d-148">4.71</span></span>    | <span data-ttu-id="8c34d-149">Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="8c34d-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="8c34d-150">Consultez la remarque 1.</span><span class="sxs-lookup"><span data-stu-id="8c34d-150">See note 1.</span></span>                                          |
| <span data-ttu-id="8c34d-151">4.72</span><span class="sxs-lookup"><span data-stu-id="8c34d-151">4.72</span></span>    | <span data-ttu-id="8c34d-152">Internet Explorer 4,01 et Windows 98.</span><span class="sxs-lookup"><span data-stu-id="8c34d-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="8c34d-153">Consultez la remarque 1.</span><span class="sxs-lookup"><span data-stu-id="8c34d-153">See note 1.</span></span>                          |
| <span data-ttu-id="8c34d-154">4,7</span><span class="sxs-lookup"><span data-stu-id="8c34d-154">4.7</span></span>     | <span data-ttu-id="8c34d-155">Internet Explorer 3. x</span><span class="sxs-lookup"><span data-stu-id="8c34d-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="8c34d-156">5.0</span><span class="sxs-lookup"><span data-stu-id="8c34d-156">5.0</span></span>     | <span data-ttu-id="8c34d-157">Microsoft Internet Explorer 5 et Windows 98 SE.</span><span class="sxs-lookup"><span data-stu-id="8c34d-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="8c34d-158">Voir la remarque 2.</span><span class="sxs-lookup"><span data-stu-id="8c34d-158">See note 2.</span></span>                |
| <span data-ttu-id="8c34d-159">5.5</span><span class="sxs-lookup"><span data-stu-id="8c34d-159">5.5</span></span>     | <span data-ttu-id="8c34d-160">Microsoft Internet Explorer 5,5 et Windows Millennium Edition (Windows Me)</span><span class="sxs-lookup"><span data-stu-id="8c34d-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="8c34d-161">6.0</span><span class="sxs-lookup"><span data-stu-id="8c34d-161">6.0</span></span>     | <span data-ttu-id="8c34d-162">Windows XP et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c34d-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="8c34d-163">**Remarque 1 :** Tous les systèmes avec Internet Explorer 4,0 ou 4,01 avaient la version associée de Shlwapi.dll (respectivement 4,71 ou 4,72).</span><span class="sxs-lookup"><span data-stu-id="8c34d-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="8c34d-164">Toutefois, pour les systèmes antérieurs à Windows 98, Internet Explorer 4,0 et 4,01 peuvent être installés avec ou sans ce qui était connu sous le nom d' *environnement intégré*.</span><span class="sxs-lookup"><span data-stu-id="8c34d-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="8c34d-165">Si Internet Explorer a été installé avec l’interpréteur de commandes intégré, la version associée de Shell32.dll (4,71 ou 4,72) a également été installée.</span><span class="sxs-lookup"><span data-stu-id="8c34d-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="8c34d-166">Si Internet Explorer a été installé sans l’interpréteur de commandes intégré, Shell32.dll est resté en version 4,0.</span><span class="sxs-lookup"><span data-stu-id="8c34d-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="8c34d-167">En d’autres termes, la présence de la version 4,71 ou 4,72 de Shlwapi.dll sur un système ne garantit pas que Shell32.dll a le même numéro de version.</span><span class="sxs-lookup"><span data-stu-id="8c34d-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="8c34d-168">Tous les systèmes Windows 98 ont la version 4,72 de Shell32.dll.</span><span class="sxs-lookup"><span data-stu-id="8c34d-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="8c34d-169">**Remarque 2 :** La version 5,0 de Shlwapi.dll a été distribuée avec Internet Explorer 5 et a été trouvée sur tous les systèmes sur lesquels Internet Explorer 5 a été installé, à l’exception de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8c34d-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="8c34d-170">La version 5,0 de Shell32.dll a été distribuée en mode natif avec Windows 2000 et Windows Millennium Edition (Windows Me), ainsi que la version 5,0 de Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="8c34d-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="8c34d-171">Utilisation de DllGetVersion pour déterminer le numéro de version</span><span class="sxs-lookup"><span data-stu-id="8c34d-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="8c34d-172">Depuis la version 4,71, les dll de l’interpréteur de commandes, entre autres, ont commencé à exporter [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="8c34d-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="8c34d-173">Cette fonction peut être appelée par une application pour déterminer la version de la DLL qui est présente sur le système.</span><span class="sxs-lookup"><span data-stu-id="8c34d-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="8c34d-174">Les dll n’exportent pas nécessairement [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="8c34d-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="8c34d-175">Testez toujours ce dernier avant de tenter de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c34d-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="8c34d-176">Pour les versions de Windows antérieures à Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) retourne une structure [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) qui contient les numéros de version principale et secondaire, le numéro de build et un ID de plateforme.</span><span class="sxs-lookup"><span data-stu-id="8c34d-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="8c34d-177">Pour les systèmes Windows 2000 et versions ultérieures, **DllGetVersion** peut retourner une structure [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="8c34d-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="8c34d-178">En plus des informations fournies via **DLLVERSIONINFO**, **DLLVERSIONINFO2** fournit également le numéro de correctif qui identifie le dernier Service Pack installé, ce qui offre un moyen plus robuste de comparer les numéros de version.</span><span class="sxs-lookup"><span data-stu-id="8c34d-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="8c34d-179">Étant donné que le premier membre de **DLLVERSIONINFO2** est une structure **DLLVERSIONINFO** , la structure la plus récente est à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="8c34d-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="8c34d-180">Utilisation de DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="8c34d-180">Using DllGetVersion</span></span>

<span data-ttu-id="8c34d-181">L’exemple de fonction suivant `GetVersion` charge une DLL spécifiée et tente d’appeler sa fonction [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="8c34d-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="8c34d-182">En cas de réussite, elle utilise une macro pour empaqueter les numéros de version majeure et mineure de la structure [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) dans une **valeur DWORD** qui est retournée à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="8c34d-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="8c34d-183">Si la DLL n’exporte pas **DllGetVersion**, la fonction retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8c34d-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="8c34d-184">Avec les systèmes Windows 2000 et versions ultérieures, vous pouvez modifier la fonction pour gérer la possibilité que **DllGetVersion** retourne une structure [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="8c34d-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="8c34d-185">Dans ce cas, utilisez les informations contenues dans le membre **ullVersion** de la structure **DLLVERSIONINFO2** pour comparer les versions, les numéros de build et les versions de Service Pack.</span><span class="sxs-lookup"><span data-stu-id="8c34d-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="8c34d-186">La macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) simplifie la tâche de comparaison de ces valeurs à celles de **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="8c34d-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="8c34d-187">L’utilisation incorrecte de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) peut poser des risques de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8c34d-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="8c34d-188">Reportez-vous à la documentation de **LoadLibrary** pour plus d’informations sur la façon de charger correctement des dll avec différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="8c34d-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


<span data-ttu-id="8c34d-189">L’exemple de code suivant montre comment vous pouvez utiliser `GetVersion` pour tester si Shell32.dll est la version 6,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8c34d-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="8c34d-190">Versions du projet</span><span class="sxs-lookup"><span data-stu-id="8c34d-190">Project Versions</span></span>

<span data-ttu-id="8c34d-191">Pour garantir la compatibilité de votre application avec différentes versions ciblées d’un fichier. dll, les macros de version sont présentes dans les fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="8c34d-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="8c34d-192">Ces macros permettent de définir, d’exclure ou de redéfinir certaines définitions pour les différentes versions de la DLL.</span><span class="sxs-lookup"><span data-stu-id="8c34d-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="8c34d-193">Pour une description détaillée de ces macros, consultez [utilisation des en-têtes Windows](../winprog/using-the-windows-headers.md) .</span><span class="sxs-lookup"><span data-stu-id="8c34d-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="8c34d-194">Par exemple, le nom de macro **\_ Win32 \_ IE** se trouve généralement dans les en-têtes plus anciens.</span><span class="sxs-lookup"><span data-stu-id="8c34d-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="8c34d-195">Vous êtes responsable de la définition de la macro sous la forme d’un nombre hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="8c34d-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="8c34d-196">Ce numéro de version définit la version cible de l’application qui utilise la DLL.</span><span class="sxs-lookup"><span data-stu-id="8c34d-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="8c34d-197">Le tableau suivant répertorie les numéros de version disponibles et l’effet de chacun d’entre eux sur votre application.</span><span class="sxs-lookup"><span data-stu-id="8c34d-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="8c34d-198">Version</span><span class="sxs-lookup"><span data-stu-id="8c34d-198">Version</span></span> | <span data-ttu-id="8c34d-199">Description</span><span class="sxs-lookup"><span data-stu-id="8c34d-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c34d-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="8c34d-200">0x0200</span></span>  | <span data-ttu-id="8c34d-201">L’application est compatible avec Shell32.dll version 4,00 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="8c34d-202">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,00.</span><span class="sxs-lookup"><span data-stu-id="8c34d-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="8c34d-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="8c34d-203">0x0300</span></span>  | <span data-ttu-id="8c34d-204">L’application est compatible avec Shell32.dll version 4,70 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="8c34d-205">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,70.</span><span class="sxs-lookup"><span data-stu-id="8c34d-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="8c34d-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="8c34d-206">0x0400</span></span>  | <span data-ttu-id="8c34d-207">L’application est compatible avec Shell32.dll version 4,71 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="8c34d-208">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,71.</span><span class="sxs-lookup"><span data-stu-id="8c34d-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="8c34d-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="8c34d-209">0x0401</span></span>  | <span data-ttu-id="8c34d-210">L’application est compatible avec Shell32.dll version 4,72 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="8c34d-211">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 4,72.</span><span class="sxs-lookup"><span data-stu-id="8c34d-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="8c34d-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="8c34d-212">0x0500</span></span>  | <span data-ttu-id="8c34d-213">L’application est compatible avec Shell32.dll et Shlwapi.dll version 5,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="8c34d-214">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,0 de Shell32.dll et Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="8c34d-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="8c34d-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="8c34d-215">0x0501</span></span>  | <span data-ttu-id="8c34d-216">L’application est compatible avec Shell32.dll et Shlwapi.dll version 5,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="8c34d-217">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 5,0 de Shell32.dll et Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="8c34d-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="8c34d-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="8c34d-218">0x0600</span></span>  | <span data-ttu-id="8c34d-219">L’application est compatible avec Shell32.dll et Shlwapi.dll version 6,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c34d-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="8c34d-220">L’application ne peut pas implémenter les fonctionnalités qui ont été ajoutées après la version 6,0 de Shell32.dll et Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="8c34d-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="8c34d-221">Si vous ne définissez pas la macro **\_ Win32 \_ IE** dans votre projet, elle est automatiquement définie en tant que 0x0500.</span><span class="sxs-lookup"><span data-stu-id="8c34d-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="8c34d-222">Pour définir une valeur différente, vous pouvez ajouter les éléments suivants aux directives de compilateur dans votre fichier Make ; Remplacez 0x0400 par le numéro de version de votre choix.</span><span class="sxs-lookup"><span data-stu-id="8c34d-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="8c34d-223">Une autre méthode consiste à ajouter une ligne semblable à la suivante dans votre code source avant d’inclure les fichiers d’en-tête de Shell.</span><span class="sxs-lookup"><span data-stu-id="8c34d-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="8c34d-224">Remplacez 0x0400 par le numéro de version de votre choix.</span><span class="sxs-lookup"><span data-stu-id="8c34d-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
