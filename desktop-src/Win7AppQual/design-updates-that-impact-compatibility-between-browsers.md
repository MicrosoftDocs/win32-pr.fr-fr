---
description: Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs
ms.assetid: F2C13FEC-5537-4B0D-BFDB-E17A42A289CB
title: Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a306a64cb03bce8b466f6367339302522109619a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088477"
---
# <a name="design-updates-that-impact-compatibility-between-browsers"></a><span data-ttu-id="e09e5-103">Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="e09e5-103">Design Updates that Impact Compatibility between Browsers</span></span>

<span data-ttu-id="e09e5-104">Cette section et le tableau suivant présentent les quatre principaux aspects de la compatibilité (pas dans l’ordre d’incidence ou de classement de priorité).</span><span class="sxs-lookup"><span data-stu-id="e09e5-104">This section and the following table show the four major areas of compatibility (not in order of incidence or ranking of priority).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e09e5-105">Modifications entre Internet Explorer 6 et Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="e09e5-105">Changes from Internet Explorer 6 to Internet Explorer 7</span></span></th>
<th><span data-ttu-id="e09e5-106">Passe d’Internet Explorer 7 à Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="e09e5-106">Changes from Internet Explorer 7 to Internet Explorer 8</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e09e5-107"><a href="versioning.md">Contrôle de version</a></span><span class="sxs-lookup"><span data-stu-id="e09e5-107"><a href="versioning.md">Versioning</a></span></span></td>
<td><ul>
<li><span data-ttu-id="e09e5-108">Vecteurs de version</span><span class="sxs-lookup"><span data-stu-id="e09e5-108">Version Vectors</span></span></li>
<li><span data-ttu-id="e09e5-109">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="e09e5-109">User Agent String</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e09e5-110">Vecteurs de version</span><span class="sxs-lookup"><span data-stu-id="e09e5-110">Version Vectors</span></span></li>
<li><span data-ttu-id="e09e5-111">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="e09e5-111">User Agent String</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e09e5-112"><a href="standards.md">Standards</a></span><span class="sxs-lookup"><span data-stu-id="e09e5-112"><a href="standards.md">Standards</a></span></span></td>
<td><ul>
<li><span data-ttu-id="e09e5-113">Améliorations apportées à HTML 4.01</span><span class="sxs-lookup"><span data-stu-id="e09e5-113">HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="e09e5-114">Améliorations apportées à CSS 2.1</span><span class="sxs-lookup"><span data-stu-id="e09e5-114">CSS 2.1 improvements</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e09e5-115">Améliorations supplémentaires apportées à HTML 4.01</span><span class="sxs-lookup"><span data-stu-id="e09e5-115">Additional HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="e09e5-116">Conformité totale à CSS 2.1</span><span class="sxs-lookup"><span data-stu-id="e09e5-116">Full CSS 2.1 compliance</span></span></li>
<li><span data-ttu-id="e09e5-117">Prise en charge partielle de HTML 5.0</span><span class="sxs-lookup"><span data-stu-id="e09e5-117">Some HTML 5.0 support</span></span></li>
<li><span data-ttu-id="e09e5-118">Prise en charge d'ECMAScript, 3ème édition, et prise en charge partielle d'ECMAScript, 5ème édition (y compris JSON natif)</span><span class="sxs-lookup"><span data-stu-id="e09e5-118">ECMAScript 3rd edition support and some ECMAScript 5th edition support (including native JSON)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e09e5-119"><a href="security.md">Sécurité</a></span><span class="sxs-lookup"><span data-stu-id="e09e5-119"><a href="security.md">Security</a></span></span></td>
<td><ul>
<li><span data-ttu-id="e09e5-120">Améliorations apportées à HTTPS</span><span class="sxs-lookup"><span data-stu-id="e09e5-120">HTTPS improvements</span></span></li>
<li><span data-ttu-id="e09e5-121">Script plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="e09e5-121">More secure scripting</span></span></li>
<li><span data-ttu-id="e09e5-122">Mode protégé (Windows Vista et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="e09e5-122">Protected Mode (Windows Vista and later versions)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e09e5-123">Meilleure protection contre les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="e09e5-123">Better protection from malware</span></span></li>
<li><span data-ttu-id="e09e5-124">Filtre DEP/NX & XSS activé par défaut</span><span class="sxs-lookup"><span data-stu-id="e09e5-124">DEP/NX & XSS filter on by default</span></span></li>
<li><span data-ttu-id="e09e5-125">Mode mixte HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="e09e5-125">HTTP/HTTPS mixed mode</span></span></li>
<li><span data-ttu-id="e09e5-126">AJAX plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="e09e5-126">AJAX more secure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e09e5-127"><a href="architecture.md">Architecture</a></span><span class="sxs-lookup"><span data-stu-id="e09e5-127"><a href="architecture.md">Architecture</a></span></span></td>

<td><ul>
<li><span data-ttu-id="e09e5-128">Internet Explorer faiblement couplé</span><span class="sxs-lookup"><span data-stu-id="e09e5-128">Loosely coupled Internet Explorer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e09e5-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e09e5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e09e5-130">Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="e09e5-130">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



