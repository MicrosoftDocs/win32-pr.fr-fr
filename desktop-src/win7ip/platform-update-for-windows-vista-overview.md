---
title: À propos de la mise à jour de plateforme pour Windows Vista
description: Fournit une vue d’ensemble de la mise à jour de la plateforme pour Windows Vista et de la mise à jour de la plateforme pour Windows Server 2008 et leurs fonctionnalités.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Mise à jour de plateforme pour Windows Server 2008
- Mise à jour de plateforme pour Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106522521"
---
# <a name="about-platform-update-for-windows-vista"></a><span data-ttu-id="56edb-105">À propos de la mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-105">About Platform Update for Windows Vista</span></span>

<span data-ttu-id="56edb-106">La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 sont des mises à jour du système d’exploitation de l’utilisateur final qui prennent en charge l’utilisation des technologies Windows 7 sélectionnées sur les versions précédentes du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-106">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 are end-user operating system updates that support the use of selected Windows 7 technologies on previous versions of the Windows operating system.</span></span> <span data-ttu-id="56edb-107">Les mises à jour incluent un ensemble de bibliothèques Runtime qui permettent aux développeurs d’applications de cibler les versions actuelles, Windows 7 et Windows Server 2008 R2, ainsi que les versions précédentes, Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-107">The updates include a set of runtime libraries that enable application developers to target current releases, Windows 7 and Windows Server 2008 R2 as well as previous versions, Windows Vista and Windows Server 2008.</span></span>

## <a name="summary-of-supported-api-by-technology"></a><span data-ttu-id="56edb-108">Résumé de l’API prise en charge par la technologie</span><span class="sxs-lookup"><span data-stu-id="56edb-108">Summary of Supported API by Technology</span></span>

<span data-ttu-id="56edb-109">Chaque technologie prise en charge par la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 mises à jour comprend un ensemble d’API qui peut être utilisé dans une application qui cible une version précédente de Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-109">Each technology that is supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008 updates includes a set of API that can be used in an application that targets previous version of Windows.</span></span>

<span data-ttu-id="56edb-110">Pour plus d’informations sur l’utilisation d’API prises en charge par les mises à jour dans une application qui cible des versions antérieures de Windows, consultez [développement d’applications pour les versions antérieures de Windows](developing-applications-for-previous-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="56edb-110">For more information about using APIs supported by the updates in an application that targets previous versions of Windows, see [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).</span></span>

> [!Note]  
> <span data-ttu-id="56edb-111">Certaines API qui sont associées à une technologie peuvent ne pas être prises en charge et le comportement, les performances ou les exigences de certaines API prises en charge peuvent varier entre les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-111">Some APIs that are associated with a technology may not be supported and the behavior, performance, or requirements for some supported APIs may vary across Windows versions.</span></span> <span data-ttu-id="56edb-112">Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.</span><span class="sxs-lookup"><span data-stu-id="56edb-112">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a><span data-ttu-id="56edb-113">Technologies prises en charge avec la mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-113">Technologies Supported with Platform Update for Windows Vista</span></span>

<span data-ttu-id="56edb-114">Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.</span><span class="sxs-lookup"><span data-stu-id="56edb-114">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="56edb-115">Les technologies prises en charge pour Windows Vista et Windows XP avec la mise à jour de plateforme pour Windows Vista sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56edb-115">The technologies that are supported for Windows Vista and Windows XP with the Platform Update for Windows Vista are shown in the following table.</span></span>

| <span data-ttu-id="56edb-116">Technology</span><span class="sxs-lookup"><span data-stu-id="56edb-116">Technology</span></span>                                                                                    | <span data-ttu-id="56edb-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-117">Windows Vista</span></span> | <span data-ttu-id="56edb-118">Windows XP</span><span class="sxs-lookup"><span data-stu-id="56edb-118">Windows XP</span></span> |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [<span data-ttu-id="56edb-119">API Windows Automation</span><span class="sxs-lookup"><span data-stu-id="56edb-119">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="56edb-120">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-120">Yes</span></span>           | <span data-ttu-id="56edb-121">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-121">Yes</span></span>        |
| [<span data-ttu-id="56edb-122">Bibliothèque Windows Graphics, Imaging et XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-122">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="56edb-123">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-123">Yes</span></span>           | <span data-ttu-id="56edb-124">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-124">No</span></span>         |
| [<span data-ttu-id="56edb-125">Bibliothèque du gestionnaire d’animations et du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-125">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="56edb-126">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-126">Yes</span></span>           | <span data-ttu-id="56edb-127">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-127">No</span></span>         |
| [<span data-ttu-id="56edb-128">Plateforme d’appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-128">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="56edb-129">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-129">Yes</span></span>           | <span data-ttu-id="56edb-130">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-130">No</span></span>         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a><span data-ttu-id="56edb-131">Technologies prises en charge avec la mise à jour de plateforme pour Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56edb-131">Technologies Supported with Platform Update for Windows Server 2008</span></span>

<span data-ttu-id="56edb-132">Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.</span><span class="sxs-lookup"><span data-stu-id="56edb-132">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="56edb-133">Les technologies prises en charge pour Windows Server 2008 et Windows Server 2003 avec la mise à jour de plateforme pour Windows Server 2008 sont présentées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56edb-133">The technologies that are supported for Windows Server 2008 and Windows Server 2003 with the Platform Update for Windows Server 2008 are shown in the following table.</span></span>

| <span data-ttu-id="56edb-134">Technology</span><span class="sxs-lookup"><span data-stu-id="56edb-134">Technology</span></span>                                                                                    | <span data-ttu-id="56edb-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56edb-135">Windows Server 2008</span></span> | <span data-ttu-id="56edb-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56edb-136">Windows Server 2003</span></span> |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [<span data-ttu-id="56edb-137">API Windows Automation</span><span class="sxs-lookup"><span data-stu-id="56edb-137">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="56edb-138">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-138">Yes</span></span>                 | <span data-ttu-id="56edb-139">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-139">Yes</span></span>                 |
| [<span data-ttu-id="56edb-140">Bibliothèque Windows Graphics, Imaging et XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-140">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="56edb-141">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-141">Yes</span></span>                 | <span data-ttu-id="56edb-142">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-142">No</span></span>                  |
| [<span data-ttu-id="56edb-143">Bibliothèque du gestionnaire d’animations et du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-143">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="56edb-144">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-144">Yes</span></span>                 | <span data-ttu-id="56edb-145">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-145">No</span></span>                  |
| [<span data-ttu-id="56edb-146">Plateforme d’appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-146">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="56edb-147">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-147">No</span></span>                  | <span data-ttu-id="56edb-148">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-148">No</span></span>                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a><span data-ttu-id="56edb-149">Descriptions des API prises en charge par la technologie</span><span class="sxs-lookup"><span data-stu-id="56edb-149">Descriptions of Supported API by Technology</span></span>

<span data-ttu-id="56edb-150">Pour plus d’informations sur l’API prise en charge pour une technologie spécifique, cliquez sur le lien dans l’une des tables de résumé pour accéder à la section relative à cette technologie.</span><span class="sxs-lookup"><span data-stu-id="56edb-150">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

-   [<span data-ttu-id="56edb-151">API Windows Automation</span><span class="sxs-lookup"><span data-stu-id="56edb-151">Windows Automation API</span></span>](#windows-automation-api)
-   [<span data-ttu-id="56edb-152">Bibliothèque Windows Graphics, Imaging et XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-152">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)
-   [<span data-ttu-id="56edb-153">Bibliothèque du gestionnaire d’animations et du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-153">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="56edb-154">Plateforme d’appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-154">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a><span data-ttu-id="56edb-155">API Windows Automation</span><span class="sxs-lookup"><span data-stu-id="56edb-155">Windows Automation API</span></span>

<span data-ttu-id="56edb-156">L’API Windows Automation 3,0 est un ensemble de dll et d’éléments d’API qui permettent aux produits de technologie d’assistance de fournir un meilleur accès informatique aux personnes qui ont des difficultés physiques ou cognitives, des handicaps ou des handicaps.</span><span class="sxs-lookup"><span data-stu-id="56edb-156">Windows Automation API 3.0 is a set of DLLs and API elements that enable Assistive Technology (AT) products to provide better computer access for individuals who have physical or cognitive difficulties, impairments, or disabilities.</span></span> <span data-ttu-id="56edb-157">En outre, étant donné que l’API Windows Automation 3,0 permet aux applications d’accéder aux éléments d’interface utilisateur d’autres applications et de les manipuler, il s’agit d’une technologie idéale pour l’implémentation d’outils de test automatisés.</span><span class="sxs-lookup"><span data-stu-id="56edb-157">Additionally, because Windows Automation API 3.0 enables applications to access and manipulate the user interface (UI) elements of other applications, it is an ideal technology for implementing automated testing tools.</span></span>

<span data-ttu-id="56edb-158">Microsoft Active Accessibility (MSAA) et UI Automation sont similaires en ce sens que les deux fournissent un moyen d’exposer et de collecter des informations sur les éléments et les contrôles de l’interface utilisateur pour prendre en charge l’accessibilité de l’interface utilisateur et l’automatisation des tests logiciels.</span><span class="sxs-lookup"><span data-stu-id="56edb-158">Microsoft Active Accessibility (MSAA) and UI Automation are similar in that both provide a means for exposing and collecting information about user interface elements and controls to support user interface accessibility and software test automation.</span></span> <span data-ttu-id="56edb-159">UI Automation est une implémentation Windows de la spécification UI Automation.</span><span class="sxs-lookup"><span data-stu-id="56edb-159">UI Automation is a Windows implementation of the UI Automation specification.</span></span> <span data-ttu-id="56edb-160">Il s’agit d’une technologie plus récente qui résout un grand nombre des limitations de MSAA.</span><span class="sxs-lookup"><span data-stu-id="56edb-160">It is a newer technology that addresses many of the limitations of MSAA.</span></span>

<span data-ttu-id="56edb-161">Pour plus d’informations sur l’API d’automatisation Windows 3,0, consultez [API Windows Automation : vue d’ensemble](/windows/desktop/WinAuto/windows-automation-api-overview).</span><span class="sxs-lookup"><span data-stu-id="56edb-161">For more information about the Windows Automation API 3.0, see [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span></span>

<span data-ttu-id="56edb-162">La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 prennent en charge l’API Windows Automation 3,0 suivante :</span><span class="sxs-lookup"><span data-stu-id="56edb-162">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 support the following Windows Automation API 3.0:</span></span>

-   [<span data-ttu-id="56edb-163">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="56edb-163">Microsoft Active Accessibility (MSAA)</span></span>](#microsoft-active-accessibility-msaa)
-   [<span data-ttu-id="56edb-164">UI Automation</span><span class="sxs-lookup"><span data-stu-id="56edb-164">UI Automation</span></span>](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="56edb-165">Éditions Windows éligibles pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-165">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="56edb-166">La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 activent la prise en charge de l’API Windows Automation 3,0 sur les éditions de Windows répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56edb-166">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Automation API 3.0 support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56edb-167">Version de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-167">Windows Version</span></span></th>
<th><span data-ttu-id="56edb-168">Éditions éligibles à la mise à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-168">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56edb-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-169">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="56edb-170">Starter avec SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="56edb-170">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="56edb-171">Édition familial de base avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-171">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-172">Édition familiale Premium avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-172">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-173">Entreprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-173">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-174">Enterprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-174">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-175">Édition intégrale avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-175">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56edb-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="56edb-176">Windows XP</span></span></td>
<td><dl> <span data-ttu-id="56edb-177">Windows XP famille avec SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="56edb-177">Windows XP Home with SP3 (x86)</span></span><br />
<span data-ttu-id="56edb-178">Windows XP Professionnel avec SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="56edb-178">Windows XP Professional with SP3 (x86)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56edb-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56edb-179">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="56edb-180">Windows Server 2008 avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-180">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56edb-181">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="56edb-181">Windows Server 2003</span></span></td>
<td><dl> <span data-ttu-id="56edb-182">Windows Server 2003 avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-182">Windows Server 2003 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a><span data-ttu-id="56edb-183">Microsoft Active Accessibility (MSAA)</span><span class="sxs-lookup"><span data-stu-id="56edb-183">Microsoft Active Accessibility (MSAA)</span></span>

<span data-ttu-id="56edb-184">Microsoft Active Accessibility (MSAA) est une technologie héritée qui a été introduite pour la première fois avec Windows 95.</span><span class="sxs-lookup"><span data-stu-id="56edb-184">Microsoft Active Accessibility (MSAA) is a legacy technology that was first introduced with Windows 95.</span></span> <span data-ttu-id="56edb-185">Il s’agit d’un ensemble d’API qui améliore la façon dont les produits de technologie d’assistance (AT) fonctionnent avec les applications qui s’exécutent sur Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-185">It is a set of APIs that improves the way Assistive Technology (AT) products work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="56edb-186">L’API fournit des interfaces et des méthodes de programmation pour exposer des informations sur les éléments de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56edb-186">The API provide programming interfaces and methods for exposing information about user interface elements.</span></span>

<span data-ttu-id="56edb-187">Pour plus d’informations sur Microsoft Active Accessibility, consultez la [Présentation technique](/windows/desktop/WinAuto/technical-overview).</span><span class="sxs-lookup"><span data-stu-id="56edb-187">For more information about Microsoft Active Accessibility, see the [Technical Overview](/windows/desktop/WinAuto/technical-overview).</span></span>

### <a name="supported-microsoft-active-accessibility-api-elements"></a><span data-ttu-id="56edb-188">Éléments de l’API Microsoft Active Accessibility pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-188">Supported Microsoft Active Accessibility API Elements</span></span>

<span data-ttu-id="56edb-189">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-189">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="ui-automation"></a><span data-ttu-id="56edb-190">Automatisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="56edb-190">UI Automation</span></span>

<span data-ttu-id="56edb-191">UI Automation est une technologie plus récente qui implémente la spécification UI Automation et résout un grand nombre des limitations de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="56edb-191">UI Automation is a newer technology that implements the UI Automation specification and addresses many of the limitations of Microsoft Active Accessibility.</span></span> <span data-ttu-id="56edb-192">Il s’agit d’un ensemble d’API qui fournit un accès par programmation aux éléments de l’interface utilisateur des applications.</span><span class="sxs-lookup"><span data-stu-id="56edb-192">It is a set of APIs that provides programmatic access to the user interface elements of applications.</span></span> <span data-ttu-id="56edb-193">L’API fournie aide les produits de technologie d’assistance et les outils de test automatisés à accéder, identifier et manipuler les éléments d’interface utilisateur standard et personnalisés d’une application.</span><span class="sxs-lookup"><span data-stu-id="56edb-193">The provided API help Assistive Technology products and automated testing tools access, identify, and manipulate the standard and custom UI elements of an application.</span></span>

<span data-ttu-id="56edb-194">Pour plus d’informations sur UI Automation, consultez [API Windows Automation : UI Automation](../winauto/entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="56edb-194">For more information about UI Automation, see [Windows Automation API: UI Automation](../winauto/entry-uiauto-win32.md).</span></span>

### <a name="supported-ui-automation-api-elements"></a><span data-ttu-id="56edb-195">Éléments d’API UI Automation pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-195">Supported UI Automation API Elements</span></span>

<span data-ttu-id="56edb-196">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-196">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-ui-automation-on-previous-windows-versions"></a><span data-ttu-id="56edb-197">Exécution d’UI Automation sur les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-197">Running UI Automation on Previous Windows Versions</span></span>

<span data-ttu-id="56edb-198">En raison des différences dans la façon dont les contrôles communs et les contrôles standard de Windows sont implémentés sur différentes versions de Windows, il peut y avoir de légères différences dans les informations que les proxys UI Automation récupèrent pour ces contrôles d’une version à l’autre.</span><span class="sxs-lookup"><span data-stu-id="56edb-198">Because of differences in how the common controls and the Windows standard controls are implemented on different Windows versions, there might be slight differences in the information that the UI Automation proxies retrieve for these controls from one version to another.</span></span>

### <a name="windows-graphics-imaging-and-xps-library"></a><span data-ttu-id="56edb-199">Bibliothèque Windows Graphics, Imaging et XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-199">Windows Graphics, Imaging and XPS Library</span></span>

<span data-ttu-id="56edb-200">La mise à jour de plateforme pour Windows Vista prend en charge les API Windows 7 suivantes à partir de la bibliothèque Windows Graphics, Imaging et XPS :</span><span class="sxs-lookup"><span data-stu-id="56edb-200">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Graphics, Imaging, and XPS Library:</span></span>

-   [<span data-ttu-id="56edb-201">Direct2D</span><span class="sxs-lookup"><span data-stu-id="56edb-201">Direct2D</span></span>](#direct2d)
-   [<span data-ttu-id="56edb-202">Direct3D</span><span class="sxs-lookup"><span data-stu-id="56edb-202">Direct3D</span></span>](#direct3d)
-   [<span data-ttu-id="56edb-203">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="56edb-203">DirectWrite</span></span>](#directwrite)
-   [<span data-ttu-id="56edb-204">Packaging</span><span class="sxs-lookup"><span data-stu-id="56edb-204">Packaging</span></span>](#packaging)
-   [<span data-ttu-id="56edb-205">Composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="56edb-205">Windows Imaging Component</span></span>](#windows-imaging-component)
-   [<span data-ttu-id="56edb-206">Document XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-206">XPS Document</span></span>](#xps-document)
-   [<span data-ttu-id="56edb-207">Impression XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-207">XPS Print</span></span>](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="56edb-208">Éditions Windows éligibles pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-208">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="56edb-209">La mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 permettent la prise en charge des graphiques Windows, d’images et de la bibliothèque XPS dans les éditions de Windows répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56edb-209">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Graphics, Imaging, and XPS Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56edb-210">Version de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-210">Windows Version</span></span></th>
<th><span data-ttu-id="56edb-211">Éditions éligibles à la mise à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-211">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56edb-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-212">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="56edb-213">Starter avec SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="56edb-213">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="56edb-214">Édition familial de base avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-214">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-215">Édition familiale Premium avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-215">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-216">Entreprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-216">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-217">Enterprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-217">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-218">Édition intégrale avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-218">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56edb-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56edb-219">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="56edb-220">Windows Server 2008 avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-220">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a><span data-ttu-id="56edb-221">Direct2D</span><span class="sxs-lookup"><span data-stu-id="56edb-221">Direct2D</span></span>

<span data-ttu-id="56edb-222">L’API Direct2D est une nouvelle API graphique en 2D en mode immédiat, accélérée par le matériel, qui offre des performances élevées et un rendu de haute qualité pour la géométrie 2D, les bitmaps et le texte.</span><span class="sxs-lookup"><span data-stu-id="56edb-222">The Direct2D API is a new hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="56edb-223">L’API Direct2D est conçue pour interagir correctement avec le code existant qui utilise GDI, GDI+ ou Direct3D.</span><span class="sxs-lookup"><span data-stu-id="56edb-223">The Direct2D API is designed to interoperate well with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="56edb-224">Pour plus d’informations sur Direct2D, consultez [à propos de Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span><span class="sxs-lookup"><span data-stu-id="56edb-224">For more information about Direct2D, see [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span></span>

### <a name="supported-direct2d-api-elements"></a><span data-ttu-id="56edb-225">Éléments de l’API Direct2D pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-225">Supported Direct2D API Elements</span></span>

<span data-ttu-id="56edb-226">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-226">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-direct2d-on-previous-windows-versions"></a><span data-ttu-id="56edb-227">Exécution de Direct2D sur les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-227">Running Direct2D on Previous Windows Versions</span></span>

<span data-ttu-id="56edb-228">Si le pilote WDDM 1,1 est manquant sur Windows Vista, les performances de l’interopérabilité de Direct2D/GDI sont dégradées.</span><span class="sxs-lookup"><span data-stu-id="56edb-228">If the WDDM 1.1 driver is missing on Windows Vista, the performance of Direct2D/GDI interoperability degrades.</span></span>

### <a name="direct3d"></a><span data-ttu-id="56edb-229">Direct3D</span><span class="sxs-lookup"><span data-stu-id="56edb-229">Direct3D</span></span>

<span data-ttu-id="56edb-230">La mise à jour de plateforme pour Windows Vista offre une prise en charge de la surface BGRA pour les chemins de code Direct3D10 et Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="56edb-230">The Platform Update for Windows Vista provides BGRA surface support for Direct3D10 and Direct3D10.1 code-paths.</span></span> <span data-ttu-id="56edb-231">Direct3D10Level9 permet aux fonctionnalités Direct3D10 de fonctionner sur du matériel Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="56edb-231">Direct3D10Level9 enables Direct3D10 functionality to work on Direct3D9 hardware.</span></span> <span data-ttu-id="56edb-232">Direct3D WARP10 est un rastériseur logiciel performant pour les applications Direct3D10.</span><span class="sxs-lookup"><span data-stu-id="56edb-232">Direct3D WARP10 is a performant software rasterizer for Direct3D10 applications.</span></span> <span data-ttu-id="56edb-233">Direct3D11, la dernière version de Direct3D, offre de nouvelles fonctionnalités, telles que la prise en charge de multithreads améliorée, la polygonalisation, la fonctionnalité de DirectCompute et la liaison de nuanceur dynamique.</span><span class="sxs-lookup"><span data-stu-id="56edb-233">Direct3D11, the latest version of Direct3D, provides new capabilities such as improved multithreading support, tessellation, DirectCompute functionality, and dynamic shader linkage.</span></span>

<span data-ttu-id="56edb-234">Si vous créez des applications qui utilisent Direct3D, le [Kit de développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) https://msdn.microsoft.com/directx/aa937788.aspx) est requis.</span><span class="sxs-lookup"><span data-stu-id="56edb-234">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required.</span></span>

<span data-ttu-id="56edb-235">Pour plus d’informations sur Direct3D, consultez [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="56edb-235">For more information about Direct3D, see [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx).</span></span>

### <a name="supported-direct3d-api-elements"></a><span data-ttu-id="56edb-236">Éléments d’API Direct3D pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-236">Supported Direct3D API Elements</span></span>

<span data-ttu-id="56edb-237">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-237">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="directwrite"></a><span data-ttu-id="56edb-238">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="56edb-238">DirectWrite</span></span>

<span data-ttu-id="56edb-239">L’API DirectWrite est une nouvelle API de texte qui fournit plusieurs couches de fonctionnalités, notamment la disposition du texte, le traitement des scripts, le rendu des glyphes et le système de polices.</span><span class="sxs-lookup"><span data-stu-id="56edb-239">The DirectWrite API is a new text API that provides multiple layers of functionality, including text layout, script processing, glyph rendering, and the font system.</span></span> <span data-ttu-id="56edb-240">DirectWrite utilise des polices OpenType et un rendu ClearType sous-pixel pour améliorer l’expérience de texte fournie par les applications.</span><span class="sxs-lookup"><span data-stu-id="56edb-240">DirectWrite uses OpenType fonts and sub-pixel ClearType rendering to enhance the text experience provided by applications.</span></span> <span data-ttu-id="56edb-241">Le rendu du texte est accéléré par le matériel lorsqu’il est utilisé avec Direct2D.</span><span class="sxs-lookup"><span data-stu-id="56edb-241">Text rendering is hardware-accelerated when used with Direct2D.</span></span>

<span data-ttu-id="56edb-242">Pour plus d’informations sur DirectWrite, consultez [Présentation de DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span><span class="sxs-lookup"><span data-stu-id="56edb-242">For more information about DirectWrite, see [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span></span>

### <a name="supported-directwrite-api-elements"></a><span data-ttu-id="56edb-243">Éléments de l’API DirectWrite pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-243">Supported DirectWrite API Elements</span></span>

<span data-ttu-id="56edb-244">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-244">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-directwrite-on-previous-windows-versions"></a><span data-ttu-id="56edb-245">Exécution de DirectWrite sur les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-245">Running DirectWrite on Previous Windows Versions</span></span>

<span data-ttu-id="56edb-246">Les problèmes de comportement suivants peuvent affecter l’utilisation de l’API DirectWrite sur les versions précédentes de Windows :</span><span class="sxs-lookup"><span data-stu-id="56edb-246">The following behavioral issues may affect the use of DirectWrite API on previous Windows versions:</span></span>

-   <span data-ttu-id="56edb-247">Les scripts de nouvelle version de Windows 7 peuvent ne pas être entièrement rendus correctement sur les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-247">Scripts new to Windows 7 may not render entirely correctly on previous Windows versions.</span></span>
-   <span data-ttu-id="56edb-248">Les paramètres régionaux non disponibles dans les versions précédentes de Windows reviennent au comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="56edb-248">Locales not available in previous Windows versions fall back to default behavior.</span></span>
-   <span data-ttu-id="56edb-249">Le tuner ClearType n’est pas disponible dans les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-249">The ClearType Tuner is not available on previous Windows versions.</span></span>
-   <span data-ttu-id="56edb-250">L’interopérabilité GDI a un coût de mémoire plus élevé dans certains scénarios sur les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-250">GDI interoperability has a higher memory cost in some scenarios on previous Windows versions.</span></span>

### <a name="packaging"></a><span data-ttu-id="56edb-251">Packaging</span><span class="sxs-lookup"><span data-stu-id="56edb-251">Packaging</span></span>

<span data-ttu-id="56edb-252">La mise à jour de plateforme pour Windows Vista prend en charge un sous-ensemble limité des API de Packaging nécessaires pour effectuer des tâches avec l’API de document XPS dans des applications non gérées.</span><span class="sxs-lookup"><span data-stu-id="56edb-252">The Platform Update for Windows Vista supports a limited subset of the Packaging APIs that are needed to perform tasks with the XPS Document API in unmanaged applications.</span></span>

<span data-ttu-id="56edb-253">Pour plus d’informations sur l’empaquetage des API, consultez [vue d’ensemble](/previous-versions/windows/desktop/opc/packaging-api-overview)de l’API de Packaging.</span><span class="sxs-lookup"><span data-stu-id="56edb-253">For more information about Packaging APIs, please see the [Packaging API Overview](/previous-versions/windows/desktop/opc/packaging-api-overview).</span></span>

### <a name="supported-packaging-api-elements"></a><span data-ttu-id="56edb-254">Éléments d’API de Packaging pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-254">Supported Packaging API Elements</span></span>

<span data-ttu-id="56edb-255">Seules les interfaces de Packaging suivantes sont prises en charge :</span><span class="sxs-lookup"><span data-stu-id="56edb-255">Only the following Packaging interfaces are supported:</span></span>

-   <span data-ttu-id="56edb-256">IOpcUri</span><span class="sxs-lookup"><span data-stu-id="56edb-256">IOpcUri</span></span>
-   <span data-ttu-id="56edb-257">IOpcPartUri</span><span class="sxs-lookup"><span data-stu-id="56edb-257">IOpcPartUri</span></span>
-   <span data-ttu-id="56edb-258">IOpcFactory (seules les méthodes suivantes sont prises en charge)</span><span class="sxs-lookup"><span data-stu-id="56edb-258">IOpcFactory (only the following methods are supported)</span></span>
    -   <span data-ttu-id="56edb-259">CreatePackageRootUri</span><span class="sxs-lookup"><span data-stu-id="56edb-259">CreatePackageRootUri</span></span>
    -   <span data-ttu-id="56edb-260">CreatePartUri</span><span class="sxs-lookup"><span data-stu-id="56edb-260">CreatePartUri</span></span>
    -   <span data-ttu-id="56edb-261">CreateStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="56edb-261">CreateStreamOnFile</span></span>

<span data-ttu-id="56edb-262">Les API de Packaging prises en charge peuvent être utilisées pour créer des flux de fichiers, ainsi que pour créer et interagir avec l’URI basé sur un package.</span><span class="sxs-lookup"><span data-stu-id="56edb-262">Supported Packaging APIs can be used to create streams over files as well as to create and interact with package-based URI.</span></span>

### <a name="running-packaging-api-on-previous-windows-versions"></a><span data-ttu-id="56edb-263">Exécution de l’API de Packaging sur les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-263">Running Packaging API on Previous Windows Versions</span></span>

<span data-ttu-id="56edb-264">Le comportement et les performances des interfaces et méthodes de Packaging prises en charge sont les mêmes sur toutes les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="56edb-264">The behavior and performance of supported Packaging interfaces and methods are the same on all supported platforms.</span></span>

<span data-ttu-id="56edb-265">Si une application tente d’instancier ou d’appeler une méthode ou une interface de Packaging non prise en charge, la tentative échoue.</span><span class="sxs-lookup"><span data-stu-id="56edb-265">If an application attempts to instantiate or call an unsupported Packaging interface or method, the attempt will fail.</span></span> <span data-ttu-id="56edb-266">Si l’appel est dirigé vers une méthode [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) non prise en charge, le \_ code d’erreur E NOTIMPL est retourné.</span><span class="sxs-lookup"><span data-stu-id="56edb-266">If the call is to an unsupported [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) method, the E\_NOTIMPL error code will be returned.</span></span>

### <a name="windows-imaging-component"></a><span data-ttu-id="56edb-267">Composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="56edb-267">Windows Imaging Component</span></span>

<span data-ttu-id="56edb-268">Les nouvelles fonctionnalités du composant WIC (Windows Imaging Component) incluent la sécurité améliorée, la prise en charge de la haute couleur et une meilleure interopérabilité des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="56edb-268">New features for the Windows Imaging Component (WIC) include enhanced security, support for high color, and better metadata interoperability.</span></span> <span data-ttu-id="56edb-269">En outre, le composant de création d’images Windows élargit sa conformité aux normes en fournissant une prise en charge du décodage de l’image progressive, des fonctionnalités PNG étendues, des métadonnées GIF,, des mises à jour de photos HD et des métadonnées qui s’étendent sur les segments APPn.</span><span class="sxs-lookup"><span data-stu-id="56edb-269">In addition, the Windows Imaging Component broadens its standards compliance by providing support for progressive image decoding, expanded PNG features, GIF metadata, , HD Photo updates, and metadata that spans APPn segments.</span></span>

<span data-ttu-id="56edb-270">Pour plus d’informations sur le composant Windows Imaging, consultez [vue d’ensemble du composant de création d’images Windows](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span><span class="sxs-lookup"><span data-stu-id="56edb-270">For more information about the Windows Imaging Component, see the [Windows Imaging Component Overview](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span></span>

### <a name="supported-wic-api-elements"></a><span data-ttu-id="56edb-271">Éléments d’API WIC pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-271">Supported WIC API Elements</span></span>

<span data-ttu-id="56edb-272">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-272">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="xps-document"></a><span data-ttu-id="56edb-273">Document XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-273">XPS Document</span></span>

<span data-ttu-id="56edb-274">Les API de document XPS prennent en charge la création, la modification et l’enregistrement de documents XPS dans des applications non gérées</span><span class="sxs-lookup"><span data-stu-id="56edb-274">The XPS Document APIs support the creating, modifying, and saving of XPS Documents in unmanaged applications</span></span>

<span data-ttu-id="56edb-275">Pour plus d’informations sur les API de document XPS, consultez le [Guide de programmation de documents XPS.](/previous-versions//dd372978(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56edb-275">For more information about XPS Document APIs, please see the [XPS Document Programming Guide.](/previous-versions//dd372978(v=vs.85))</span></span>

### <a name="supported-xps-document-api-elements"></a><span data-ttu-id="56edb-276">Éléments de l’API document XPS pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-276">Supported XPS Document API Elements</span></span>

<span data-ttu-id="56edb-277">Seules les interfaces de [signature numérique XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) ne sont pas prises en charge sur les versions de système d’exploitation de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="56edb-277">Only the [XPS Digital Signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) interfaces are not supported on down-level OS versions.</span></span>

### <a name="xps-print"></a><span data-ttu-id="56edb-278">Impression XPS</span><span class="sxs-lookup"><span data-stu-id="56edb-278">XPS Print</span></span>

<span data-ttu-id="56edb-279">Les API d’impression XPS prennent en charge l’impression de documents XPS à partir d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-279">The XPS Print APIs support the printing of XPS documents from Windows-based applications.</span></span>

<span data-ttu-id="56edb-280">Pour plus d’informations sur les API d’impression XPS, consultez l' [API XpsPrint](/windows/desktop/printdocs/xpsprint-api).</span><span class="sxs-lookup"><span data-stu-id="56edb-280">For more information about XPS Print APIs, please see the [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).</span></span>

### <a name="supported-xps-print-api-elements"></a><span data-ttu-id="56edb-281">Éléments de l’API d’impression XPS pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-281">Supported XPS Print API Elements</span></span>

<span data-ttu-id="56edb-282">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-282">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-ribbon-and-animation-manager-library"></a><span data-ttu-id="56edb-283">Bibliothèque du gestionnaire d’animations et du ruban Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-283">Windows Ribbon and Animation Manager Library</span></span>

<span data-ttu-id="56edb-284">La mise à jour de plateforme pour Windows Vista prend en charge les API Windows 7 suivantes à partir du ruban Windows et de la bibliothèque d’animation :</span><span class="sxs-lookup"><span data-stu-id="56edb-284">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Ribbon and Animation Library:</span></span>

-   [<span data-ttu-id="56edb-285">Infrastructure de ruban Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-285">Windows Ribbon Framework</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="56edb-286">Gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-286">Windows Animation Manager</span></span>](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="56edb-287">Éditions Windows éligibles pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-287">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="56edb-288">La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 activent la prise en charge de la bibliothèque du gestionnaire d’animations et du ruban Windows dans les éditions de Windows répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56edb-288">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Ribbon and Animation Manager Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56edb-289">Version de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-289">Windows Version</span></span></th>
<th><span data-ttu-id="56edb-290">Éditions éligibles à la mise à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-290">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56edb-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-291">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="56edb-292">Starter avec SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="56edb-292">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="56edb-293">Édition familial de base avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-293">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-294">Édition familiale Premium avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-294">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-295">Entreprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-295">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-296">Enterprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-296">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-297">Édition intégrale avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-297">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56edb-298">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56edb-298">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="56edb-299">Windows Server 2008 avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-299">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a><span data-ttu-id="56edb-300">Infrastructure de ruban Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-300">Windows Ribbon Framework</span></span>

<span data-ttu-id="56edb-301">L’infrastructure de ruban Windows (ruban) est un système de présentation de commande riche qui offre une alternative moderne aux menus en couches, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="56edb-301">The Windows Ribbon (Ribbon) framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

<span data-ttu-id="56edb-302">L’infrastructure est une collection d’API Microsoft Win32 qui fournissent une série de nouvelles fonctionnalités d’interface utilisateur pour les développeurs Windows et comprend à la fois le ruban et un système de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="56edb-302">The framework is a collection of Microsoft Win32 APIs that provide a host of new user interface capabilities for Windows developers and includes both the Ribbon and a context menu system.</span></span>

<span data-ttu-id="56edb-303">Pour plus d’informations sur l’infrastructure du ruban, consultez [Présentation de l’infrastructure du ruban Windows](../windowsribbon/windowsribbon-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="56edb-303">For more information about the Ribbon framework, see [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span></span>

### <a name="supported-ribbon-framework-api-elements"></a><span data-ttu-id="56edb-304">Éléments d’API Framework du ruban pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-304">Supported Ribbon Framework API Elements</span></span>

<span data-ttu-id="56edb-305">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-305">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-animation-manager"></a><span data-ttu-id="56edb-306">Gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-306">Windows Animation Manager</span></span>

<span data-ttu-id="56edb-307">Le gestionnaire d’animations Windows (animation Windows) est une interface de programmation qui prend en charge l’animation des éléments visuels des applications Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-307">The Windows Animation Manager (Windows Animation) is a programmatic interface that supports the animation of visual elements of Windows applications.</span></span> <span data-ttu-id="56edb-308">L’animation Windows est conçue pour simplifier le développement et la maintenance des séquences d’animation et permettre aux développeurs d’implémenter des animations cohérentes et intuitives.</span><span class="sxs-lookup"><span data-stu-id="56edb-308">Windows Animation is designed to simplify the development and maintenance of animation sequences and to enable developers to implement animations that are consistent and intuitive.</span></span> <span data-ttu-id="56edb-309">L’animation Windows peut être utilisée avec n’importe quelle plateforme graphique, notamment Direct2D, Direct3D ou GDI+.</span><span class="sxs-lookup"><span data-stu-id="56edb-309">Windows Animation can be used with any graphics platform including Direct2D, Direct3D, or GDI+.</span></span>

<span data-ttu-id="56edb-310">Windows animation est une API COM à thread unique qui fournit tout ce dont un développeur a besoin pour créer, gérer et générer des animations d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56edb-310">Windows Animation is a single-threaded COM API that provides everything a developer needs to create, manage, and drive UI animation.</span></span>

<span data-ttu-id="56edb-311">Pour plus d’informations sur le gestionnaire d’animations Windows, consultez Présentation de l' [Animation Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span><span class="sxs-lookup"><span data-stu-id="56edb-311">For more information about the Windows Animation Manager, see [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span></span>

### <a name="supported-animation-manager-api-elements"></a><span data-ttu-id="56edb-312">Éléments de l’API du gestionnaire d’animations pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-312">Supported Animation Manager API Elements</span></span>

<span data-ttu-id="56edb-313">Toutes les API sont prises en charge dans les versions précédentes de Windows qui sont éligibles à la mise à jour de plateforme pour Windows Vista ou à la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="56edb-313">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-portable-devices-platform"></a><span data-ttu-id="56edb-314">Plateforme d’appareils mobiles Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-314">Windows Portable Devices Platform</span></span>

<span data-ttu-id="56edb-315">La mise à jour de plateforme pour Windows Vista prend en charge les extensions Windows 7 sur la plateforme Windows Mobile Devices (WPD).</span><span class="sxs-lookup"><span data-stu-id="56edb-315">The Platform Update for Windows Vista supports the Windows 7 extensions to the Windows Portable Devices (WPD) platform.</span></span> <span data-ttu-id="56edb-316">Cette fonctionnalité permet aux ordinateurs de communiquer avec les périphériques de stockage et les supports associés.</span><span class="sxs-lookup"><span data-stu-id="56edb-316">This feature enables computers to communicate with attached media and storage devices.</span></span> <span data-ttu-id="56edb-317">WPD offre une méthode flexible et fiable pour les ordinateurs qui communiquent avec les appareils photo numériques, les lecteurs musicaux, les téléphones mobiles et de nombreux autres types d’appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="56edb-317">WPD provides a flexible, robust way for computers to communicate with digital cameras, music players, mobile phones, and many other types of connected devices.</span></span>

<span data-ttu-id="56edb-318">Pour plus d’informations sur les appareils mobiles Windows, consultez [appareils mobiles Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .</span><span class="sxs-lookup"><span data-stu-id="56edb-318">For more information about Windows Portable Devices, see [Windows Portable Devices](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/).</span></span>

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="56edb-319">Éditions Windows éligibles pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-319">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="56edb-320">La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 activent la prise en charge des appareils mobiles Windows (WPD) sur les éditions de Windows répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56edb-320">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Portable Devices (WPD) support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56edb-321">Version de Windows</span><span class="sxs-lookup"><span data-stu-id="56edb-321">Windows Version</span></span></th>
<th><span data-ttu-id="56edb-322">Éditions éligibles à la mise à jour</span><span class="sxs-lookup"><span data-stu-id="56edb-322">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56edb-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-323">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="56edb-324">Starter avec SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="56edb-324">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="56edb-325">Édition familial de base avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-325">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-326">Édition familiale Premium avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-326">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-327">Entreprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-327">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-328">Enterprise avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-328">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="56edb-329">Édition intégrale avec SP2 (x86 et amd64)</span><span class="sxs-lookup"><span data-stu-id="56edb-329">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a><span data-ttu-id="56edb-330">Éléments d’API WPD pris en charge</span><span class="sxs-lookup"><span data-stu-id="56edb-330">Supported WPD API Elements</span></span>

<span data-ttu-id="56edb-331">Le tableau suivant identifie les fonctionnalités prises en charge pour les versions Windows 7, Windows Vista et Windows Vista avec la mise à jour de plateforme pour Windows Vista du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="56edb-331">The following table identifies the features that are supported for the Windows 7, Windows Vista, and Windows Vista with Platform Update for Windows Vista versions of the Windows operating system.</span></span>

| <span data-ttu-id="56edb-332">Fonctionnalité WPD</span><span class="sxs-lookup"><span data-stu-id="56edb-332">WPD Feature</span></span>                    | <span data-ttu-id="56edb-333">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56edb-333">Windows 7</span></span> | <span data-ttu-id="56edb-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-334">Windows Vista</span></span> | <span data-ttu-id="56edb-335">Windows Vista avec la mise à jour de la plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-335">Windows Vista with Platform Update for Windows Vista</span></span> |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| <span data-ttu-id="56edb-336">MTP sur USB</span><span class="sxs-lookup"><span data-stu-id="56edb-336">MTP over USB</span></span>                   | <span data-ttu-id="56edb-337">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-337">Yes</span></span>       | <span data-ttu-id="56edb-338">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-338">Yes</span></span>           | <span data-ttu-id="56edb-339">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-339">Yes</span></span>                                                  |
| <span data-ttu-id="56edb-340">MTP sur IP</span><span class="sxs-lookup"><span data-stu-id="56edb-340">MTP over IP</span></span>                    | <span data-ttu-id="56edb-341">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-341">Yes</span></span>       | <span data-ttu-id="56edb-342">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-342">Yes</span></span>           | <span data-ttu-id="56edb-343">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-343">Yes</span></span>                                                  |
| <span data-ttu-id="56edb-344">MTP sur Bluetooth</span><span class="sxs-lookup"><span data-stu-id="56edb-344">MTP over Bluetooth</span></span>             | <span data-ttu-id="56edb-345">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-345">Yes</span></span>       | <span data-ttu-id="56edb-346">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-346">No</span></span>            | <span data-ttu-id="56edb-347">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-347">Yes</span></span>                                                  |
| <span data-ttu-id="56edb-348">Services d’appareil WPD et MTP</span><span class="sxs-lookup"><span data-stu-id="56edb-348">WPD and MTP Device Services</span></span>    | <span data-ttu-id="56edb-349">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-349">Yes</span></span>       | <span data-ttu-id="56edb-350">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-350">No</span></span>            | <span data-ttu-id="56edb-351">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-351">Yes</span></span>                                                  |
| <span data-ttu-id="56edb-352">Automation WPD</span><span class="sxs-lookup"><span data-stu-id="56edb-352">WPD Automation</span></span>                 | <span data-ttu-id="56edb-353">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-353">Yes</span></span>       | <span data-ttu-id="56edb-354">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-354">No</span></span>            | <span data-ttu-id="56edb-355">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-355">No</span></span>                                                   |
| <span data-ttu-id="56edb-356">Multi-fonctions/transport multiple</span><span class="sxs-lookup"><span data-stu-id="56edb-356">Multi-function/Multi-transport</span></span> | <span data-ttu-id="56edb-357">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-357">Yes</span></span>       | <span data-ttu-id="56edb-358">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-358">No</span></span>            | <span data-ttu-id="56edb-359">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-359">No</span></span>                                                   |
| <span data-ttu-id="56edb-360">Device Stage</span><span class="sxs-lookup"><span data-stu-id="56edb-360">Device Stage</span></span>                   | <span data-ttu-id="56edb-361">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-361">Yes</span></span>       | <span data-ttu-id="56edb-362">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-362">No</span></span>            | <span data-ttu-id="56edb-363">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-363">No</span></span>                                                   |
| <span data-ttu-id="56edb-364">Plateforme de synchronisation des appareils</span><span class="sxs-lookup"><span data-stu-id="56edb-364">Device Sync Platform</span></span>           | <span data-ttu-id="56edb-365">Oui</span><span class="sxs-lookup"><span data-stu-id="56edb-365">Yes</span></span>       | <span data-ttu-id="56edb-366">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-366">No</span></span>            | <span data-ttu-id="56edb-367">Non</span><span class="sxs-lookup"><span data-stu-id="56edb-367">No</span></span>                                                   |



 

<span data-ttu-id="56edb-368">Pour les éditions de Windows 7 et Windows Vista sur lesquelles le lecteur Microsoft Windows Media n’est pas installé par défaut (les éditions N et KN), vous devez installer le [Kit de développement logiciel (SDK) du format Windows Media 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) pour activer la fonctionnalité wpd).</span><span class="sxs-lookup"><span data-stu-id="56edb-368">For editions of Windows 7 and Windows Vista that do not have Microsoft Windows Media Player installed by default (the N and KN editions), you must install the [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) to enable WPD functionality.</span></span> <span data-ttu-id="56edb-369">Pour plus d’informations, consultez l’article de la [base de connaissances](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , qui a été publié à l’origine en tant que solution pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56edb-369">For more information, see the [Knowledge Base article](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715), which was originally published as a resolution for Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56edb-370">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56edb-370">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56edb-371">Mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-371">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="56edb-372">**Vues d'ensemble**</span><span class="sxs-lookup"><span data-stu-id="56edb-372">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="56edb-373">À propos de la mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56edb-373">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="56edb-374">Article de la base de connaissances sur la mise à jour de plateforme pour Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="56edb-374">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 