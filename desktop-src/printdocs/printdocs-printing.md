---
description: Windows fournit aux applications un ensemble complet de fonctions qui permettent l’impression sur différents appareils, tels que les imprimantes laser, les traceurs vectorisés, les imprimantes raster et les télécopieurs.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impression (documents et impression)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522069"
---
# <a name="printing-documents-and-printing"></a><span data-ttu-id="34931-103">Impression (documents et impression)</span><span class="sxs-lookup"><span data-stu-id="34931-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="34931-104">Windows fournit aux applications un ensemble complet de fonctions qui permettent l’impression sur différents appareils, tels que les imprimantes laser, les traceurs vectorisés, les imprimantes raster et les télécopieurs.</span><span class="sxs-lookup"><span data-stu-id="34931-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="34931-105">Impression d’applications de bureau</span><span class="sxs-lookup"><span data-stu-id="34931-105">Desktop App Printing</span></span>

<span data-ttu-id="34931-106">Les programmeurs Windows peuvent choisir parmi plusieurs technologies différentes pour imprimer à partir de leur application.</span><span class="sxs-lookup"><span data-stu-id="34931-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34931-107">Technology</span><span class="sxs-lookup"><span data-stu-id="34931-107">Technology</span></span></th>
<th><span data-ttu-id="34931-108">Description</span><span class="sxs-lookup"><span data-stu-id="34931-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34931-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">API d’impression de package de document</a></span><span class="sxs-lookup"><span data-stu-id="34931-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="34931-110">Fournit une interface qui permet à une application d’accéder au package de documents d’impression et de le gérer.</span><span class="sxs-lookup"><span data-stu-id="34931-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="34931-111">Cette API est disponible avec Windows 8 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="34931-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34931-112"><a href="print-spooler-api.md">API du spouleur d’impression</a></span><span class="sxs-lookup"><span data-stu-id="34931-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="34931-113">Fournit une interface au spouleur d’impression pour permettre aux applications de gérer les imprimantes et les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="34931-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="34931-114">Les applications utilisent l' <a href="print-spooler-api.md">API spouleur d’impression</a> pour démarrer, arrêter, contrôler et configurer les travaux d’impression gérés par le spouleur d’impression, qu’ils utilisent l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API imprimer le package de document</a> ou l’API d' <a href="gdi-printing.md">impression GDI</a> pour imprimer le contenu.</span><span class="sxs-lookup"><span data-stu-id="34931-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34931-115"><a href="print-ticket-api.md">API ticket d’impression</a></span><span class="sxs-lookup"><span data-stu-id="34931-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="34931-116">Fournit aux applications des fonctions permettant de gérer et de convertir les tickets d’impression.</span><span class="sxs-lookup"><span data-stu-id="34931-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34931-117"><a href="gdi-printing.md">API d’impression GDI</a></span><span class="sxs-lookup"><span data-stu-id="34931-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="34931-118">Fournit des applications avec une interface d’impression indépendante du périphérique.</span><span class="sxs-lookup"><span data-stu-id="34931-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="34931-119">Les développeurs qui écrivent des applications pour Windows Vista et les versions ultérieures de Windows doivent envisager d’utiliser l' <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de document XPS</a> dans leur application.</span><span class="sxs-lookup"><span data-stu-id="34931-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="34931-120">L' <a href="gdi-printing.md">API d’impression GDI</a> convient aux applications qui doivent s’exécuter sur Windows XP et les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="34931-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="34931-121">L’illustration suivante fournit une vue d’ensemble de la façon dont les différentes API d’impression sont liées.</span><span class="sxs-lookup"><span data-stu-id="34931-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![diagramme qui montre comment une application Windows Native peut utiliser les API d’impression](images/print-apis.png)

 

<span data-ttu-id="34931-123">L' [API d’impression de package de document](./tailored-app-printing-api.md)dans cette section décrit les interfaces imprimer le package de document et aperçu avant impression que vous pouvez utiliser avec Windows 8 et les versions ultérieures de Windows Desktop.</span><span class="sxs-lookup"><span data-stu-id="34931-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="34931-124">Pour plus d’informations sur l’impression à partir d’applications du Windows Store écrites en JavaScript et HTML, consultez [impression (applications du Windows Store en JavaScript et html)](/previous-versions/windows/apps/hh465225(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="34931-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="34931-125">Pour plus d’informations sur l’impression à partir d’applications du Windows Store écrites en C#, Microsoft Visual Basic ou C++ et XAML, consultez [impression (applications du Windows Store en C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="34931-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="34931-126">Pour obtenir la liste des API d’impression d’applications de bureau qui peuvent également être utilisées dans les applications du Windows Store, consultez [Win32 et com pour les applications du Windows Store (impression et documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) .</span><span class="sxs-lookup"><span data-stu-id="34931-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="34931-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="34931-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="34931-128">[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34931-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="34931-129">Communications d’imprimante bidirectionnelles (Centre de développement matériel)</span><span class="sxs-lookup"><span data-stu-id="34931-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

