---
description: Ces rubriques décrivent les documents et les fonctionnalités d’impression de Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: Documents et impression
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535116"
---
# <a name="documents-and-printing"></a><span data-ttu-id="daeef-103">Documents et impression</span><span class="sxs-lookup"><span data-stu-id="daeef-103">Documents and Printing</span></span>

<span data-ttu-id="daeef-104">Ces rubriques décrivent les documents et les fonctionnalités d’impression de Windows qui permettent aux applications d’enregistrer, d’afficher et d’imprimer.</span><span class="sxs-lookup"><span data-stu-id="daeef-104">These topics describe the documents and printing features of Windows that enable applications to save, view, and print.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="daeef-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="daeef-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daeef-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="daeef-106">Topic</span></span></th>
<th><span data-ttu-id="daeef-107">Description</span><span class="sxs-lookup"><span data-stu-id="daeef-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="daeef-108"><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Nouveautés pour l’impression</a></span><span class="sxs-lookup"><span data-stu-id="daeef-108"><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">What's New for Printing</a></span></span><br/></td>
<td><span data-ttu-id="daeef-109">Windows 8 prend en charge <a href="/previous-versions/windows/apps/hh465225(v=win.10)">l’impression pour les applications du Windows Store en JavaScript et html</a> , et <a href="/previous-versions/windows/apps/hh465196(v=win.10)">l’impression pour les applications du Windows Store en C#/VB/C + + et XAML</a>.</span><span class="sxs-lookup"><span data-stu-id="daeef-109">Windows 8 supports <a href="/previous-versions/windows/apps/hh465225(v=win.10)">printing for Windows Store apps using JavaScript and HTML</a> and <a href="/previous-versions/windows/apps/hh465196(v=win.10)">printing for Windows Store apps using C#/VB/C++ and XAML</a>.</span></span><br/> <span data-ttu-id="daeef-110">Windows 8 inclut également une nouvelle API basée sur COM qui offre une prise en charge complète d’Open XPS et l’accès aux parties des nouveaux pilotes d’imprimante pris en charge par Windows 8.</span><span class="sxs-lookup"><span data-stu-id="daeef-110">Windows 8 also includes a new COM-based API that provides full support for Open XPS and access to portions of the new printer drivers that Windows 8 supports.</span></span> <span data-ttu-id="daeef-111">Pour plus d’informations sur la nouvelle API, consultez <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print document package API</a>.</span><span class="sxs-lookup"><span data-stu-id="daeef-111">For more information about the new API, see <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.</span></span><br/> <span data-ttu-id="daeef-112">Le programme de boîte de réception du pilote d’impression Windows vérifie que Windows 8 prend en charge un pourcentage élevé des imprimantes populaires.</span><span class="sxs-lookup"><span data-stu-id="daeef-112">The Windows Print Driver Inbox Program makes sure that Windows 8 includes support for a high percentage of the popular printers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daeef-113"><a href="/windows/desktop/printdocs/jobbindalldocuments">Documents XPS</a></span><span class="sxs-lookup"><span data-stu-id="daeef-113"><a href="/windows/desktop/printdocs/jobbindalldocuments">XPS Documents</a></span></span><br/></td>
<td><span data-ttu-id="daeef-114">Informations sur l’API de document XPS d’une signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="daeef-114">Information about the XPS Document API an XPS Digital Signatures.</span></span><br/>
<ul>
<li><span data-ttu-id="daeef-115"><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de document XPS</a></span><span class="sxs-lookup"><span data-stu-id="daeef-115"><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a></span></span><br/> <span data-ttu-id="daeef-116">L’API de document XPS est une API Windows native qui prend en charge le modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="daeef-116">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="daeef-117">L’API de document XPS a été introduite dans Windows 7 et peut être utilisée dans les programmes en mode utilisateur et les pilotes d’imprimante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="daeef-117">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span><br/></li>
<li><span data-ttu-id="daeef-118"><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API de signature numérique XPS</a></span><span class="sxs-lookup"><span data-stu-id="daeef-118"><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">XPS Digital Signature API</a></span></span><br/> <span data-ttu-id="daeef-119">Les signatures numériques XPS activent la signature de documents, la vérification de l’identité du signataire et indiquent si un document XPS a été modifié depuis sa signature.</span><span class="sxs-lookup"><span data-stu-id="daeef-119">XPS Digital Signatures enable document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daeef-120"><a href="printdocs-printing.md">Impression</a></span><span class="sxs-lookup"><span data-stu-id="daeef-120"><a href="printdocs-printing.md">Printing</a></span></span><br/></td>
<td><span data-ttu-id="daeef-121">Informations sur les fonctionnalités d’impression prises en charge par Windows.</span><span class="sxs-lookup"><span data-stu-id="daeef-121">Information about the printing features supported by Windows.</span></span> <span data-ttu-id="daeef-122">Ces fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="daeef-122">These features include:</span></span><br/>
<ul>
<li><span data-ttu-id="daeef-123"><a href="/windows/desktop/printdocs/tailored-app-printing-api">API d’impression de package de document</a></span><span class="sxs-lookup"><span data-stu-id="daeef-123"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/> <span data-ttu-id="daeef-124">Fournit aux applications une interface qui permet la gestion du package <strong>PrintDocument</strong> .</span><span class="sxs-lookup"><span data-stu-id="daeef-124">Provides apps with an interface that allows the management of the <strong>PrintDocument</strong> package.</span></span><br/></li>
<li><span data-ttu-id="daeef-125"><a href="print-spooler-api.md">API du spouleur d’impression</a></span><span class="sxs-lookup"><span data-stu-id="daeef-125"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/> <span data-ttu-id="daeef-126">Fournit une interface au spouleur d’impression pour permettre aux applications de gérer les imprimantes et les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="daeef-126">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/></li>
<li><span data-ttu-id="daeef-127"><a href="print-ticket-api.md">API ticket d’impression</a></span><span class="sxs-lookup"><span data-stu-id="daeef-127"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/> <span data-ttu-id="daeef-128">Fournit aux applications des fonctions permettant de gérer et de convertir les tickets d’impression.</span><span class="sxs-lookup"><span data-stu-id="daeef-128">Provides applications with functions to manage and convert print tickets.</span></span><br/></li>
<li><span data-ttu-id="daeef-129"><a href="gdi-printing.md">API d’impression GDI</a></span><span class="sxs-lookup"><span data-stu-id="daeef-129"><a href="gdi-printing.md">GDI Print API</a></span></span><br/> <span data-ttu-id="daeef-130">Fournit des applications avec une interface d’impression indépendante du périphérique.</span><span class="sxs-lookup"><span data-stu-id="daeef-130">Provides applications with a device-independent printing interface.</span></span> <br/></li>
<li><p><span data-ttu-id="daeef-131"><a href="xps-printing.md">API d’impression XPS</a></span><span class="sxs-lookup"><span data-stu-id="daeef-131"><a href="xps-printing.md">XPS Print API</a></span></span><br/> <span data-ttu-id="daeef-132">Fournit une interface au spouleur d’impression que les applications peuvent utiliser pour envoyer des documents XPS à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="daeef-132">Provides an interface to the print spooler that applications can use to send XPS documents to a printer.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="daeef-133">L’API d’impression XPS n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="daeef-133">The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="daeef-134">Les applications clientes doivent utiliser l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API Print document package</a> à la place.</span><span class="sxs-lookup"><span data-stu-id="daeef-134">Client applications should use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> instead.</span></span>
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daeef-135"><a href="/windows/desktop/printdocs/printschema">Schéma d’impression</a></span><span class="sxs-lookup"><span data-stu-id="daeef-135"><a href="/windows/desktop/printdocs/printschema">Print Schema</a></span></span><br/></td>
<td><span data-ttu-id="daeef-136">Le schéma d’impression et les technologies associées décrivent les fonctionnalités d’une imprimante et spécifient les préférences d’impression d’un document pour les imprimantes et l’affichage des applications.</span><span class="sxs-lookup"><span data-stu-id="daeef-136">The Print Schema and related technologies describe a printer's features and specify the printing preferences of a document to printers and viewing applications.</span></span> <span data-ttu-id="daeef-137">La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a> est un document téléchargeable qui contient des informations sur le schéma d’impression et comment l’utiliser dans des documents et l’impression.</span><span class="sxs-lookup"><span data-stu-id="daeef-137">The <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a> is a downloadable document that contains information about the Print Schema and how to use it in documents and printing.</span></span> <span data-ttu-id="daeef-138">Les informations en ligne qui se trouvent dans cette section sont fournies uniquement à titre d’information et peuvent ne pas refléter avec précision la version actuelle de la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a>.</span><span class="sxs-lookup"><span data-stu-id="daeef-138">The online information that is found in this section is provided for your information only and might not accurately reflect the current version of the <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a>.</span></span><br/> <span data-ttu-id="daeef-139">Reportez-vous à la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">spécification du schéma d’impression</a> pour obtenir les informations de conception les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="daeef-139">Refer to the <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a> for the most current design information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a><span data-ttu-id="daeef-140">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="daeef-140">Additional resources</span></span>

<span data-ttu-id="daeef-141">L' [exemple d’application Print](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) montre comment imprimer à partir d’une application du Windows Store à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="daeef-141">The [Print Sample sample app](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) demonstrates how to print from a Windows Store app starting with Windows 8.</span></span>

<span data-ttu-id="daeef-142">Les fonctionnalités décrites dans cette section concernent la programmation Windows native.</span><span class="sxs-lookup"><span data-stu-id="daeef-142">The features described in this section are for native Windows programming.</span></span> <span data-ttu-id="daeef-143">Pour utiliser des fonctionnalités similaires dans la programmation .NET (managée), consultez [Windows Presentation Foundation des documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="daeef-143">To use similar features in .NET (managed) programming, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

<span data-ttu-id="daeef-144">Les documents XPS sont basés sur l’API de [Packaging](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="daeef-144">XPS documents are built on the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="daeef-145">Pour plus d’accès au contenu d’un document XPS, consultez l’API Packaging.</span><span class="sxs-lookup"><span data-stu-id="daeef-145">See the Packaging API, for lower level access to the contents of an XPS document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daeef-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="daeef-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daeef-147">Communications d’imprimante bidirectionnelles (Centre de développement matériel)</span><span class="sxs-lookup"><span data-stu-id="daeef-147">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
