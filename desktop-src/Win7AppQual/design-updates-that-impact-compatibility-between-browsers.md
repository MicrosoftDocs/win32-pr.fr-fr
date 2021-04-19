---
description: .
ms.assetid: F2C13FEC-5537-4B0D-BFDB-E17A42A289CB
title: Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da217d761a603e2edf8f799ab638561b357151c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525724"
---
# <a name="design-updates-that-impact-compatibility-between-browsers"></a><span data-ttu-id="ce4db-103">Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="ce4db-103">Design Updates that Impact Compatibility between Browsers</span></span>

<span data-ttu-id="ce4db-104">Cette section et le tableau suivant présentent les quatre principaux aspects de la compatibilité (pas dans l’ordre d’incidence ou de classement de priorité).</span><span class="sxs-lookup"><span data-stu-id="ce4db-104">This section and the following table show the four major areas of compatibility (not in order of incidence or ranking of priority).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ce4db-105">Modifications entre Internet Explorer 6 et Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="ce4db-105">Changes from Internet Explorer 6 to Internet Explorer 7</span></span></th>
<th><span data-ttu-id="ce4db-106">Passe d’Internet Explorer 7 à Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="ce4db-106">Changes from Internet Explorer 7 to Internet Explorer 8</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce4db-107"><a href="versioning.md">Contrôle de version</a></span><span class="sxs-lookup"><span data-stu-id="ce4db-107"><a href="versioning.md">Versioning</a></span></span></td>
<td><ul>
<li><span data-ttu-id="ce4db-108">Vecteurs de version</span><span class="sxs-lookup"><span data-stu-id="ce4db-108">Version Vectors</span></span></li>
<li><span data-ttu-id="ce4db-109">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="ce4db-109">User Agent String</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ce4db-110">Vecteurs de version</span><span class="sxs-lookup"><span data-stu-id="ce4db-110">Version Vectors</span></span></li>
<li><span data-ttu-id="ce4db-111">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="ce4db-111">User Agent String</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce4db-112"><a href="standards.md">Standards</a></span><span class="sxs-lookup"><span data-stu-id="ce4db-112"><a href="standards.md">Standards</a></span></span></td>
<td><ul>
<li><span data-ttu-id="ce4db-113">Améliorations apportées à HTML 4.01</span><span class="sxs-lookup"><span data-stu-id="ce4db-113">HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="ce4db-114">Améliorations apportées à CSS 2.1</span><span class="sxs-lookup"><span data-stu-id="ce4db-114">CSS 2.1 improvements</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ce4db-115">Améliorations supplémentaires apportées à HTML 4.01</span><span class="sxs-lookup"><span data-stu-id="ce4db-115">Additional HTML 4.01 improvements</span></span></li>
<li><span data-ttu-id="ce4db-116">Conformité totale à CSS 2.1</span><span class="sxs-lookup"><span data-stu-id="ce4db-116">Full CSS 2.1 compliance</span></span></li>
<li><span data-ttu-id="ce4db-117">Prise en charge partielle de HTML 5.0</span><span class="sxs-lookup"><span data-stu-id="ce4db-117">Some HTML 5.0 support</span></span></li>
<li><span data-ttu-id="ce4db-118">Prise en charge d'ECMAScript, 3ème édition, et prise en charge partielle d'ECMAScript, 5ème édition (y compris JSON natif)</span><span class="sxs-lookup"><span data-stu-id="ce4db-118">ECMAScript 3rd edition support and some ECMAScript 5th edition support (including native JSON)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce4db-119"><a href="security.md">Sécurité</a></span><span class="sxs-lookup"><span data-stu-id="ce4db-119"><a href="security.md">Security</a></span></span></td>
<td><ul>
<li><span data-ttu-id="ce4db-120">Améliorations apportées à HTTPS</span><span class="sxs-lookup"><span data-stu-id="ce4db-120">HTTPS improvements</span></span></li>
<li><span data-ttu-id="ce4db-121">Script plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="ce4db-121">More secure scripting</span></span></li>
<li><span data-ttu-id="ce4db-122">Mode protégé (Windows Vista et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="ce4db-122">Protected Mode (Windows Vista and later versions)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ce4db-123">Meilleure protection contre les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="ce4db-123">Better protection from malware</span></span></li>
<li><span data-ttu-id="ce4db-124">Filtre DEP/NX & XSS activé par défaut</span><span class="sxs-lookup"><span data-stu-id="ce4db-124">DEP/NX & XSS filter on by default</span></span></li>
<li><span data-ttu-id="ce4db-125">Mode mixte HTTP/HTTPS</span><span class="sxs-lookup"><span data-stu-id="ce4db-125">HTTP/HTTPS mixed mode</span></span></li>
<li><span data-ttu-id="ce4db-126">AJAX plus sécurisé</span><span class="sxs-lookup"><span data-stu-id="ce4db-126">AJAX more secure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce4db-127"><a href="architecture.md">Architecture</a></span><span class="sxs-lookup"><span data-stu-id="ce4db-127"><a href="architecture.md">Architecture</a></span></span></td>

<td><ul>
<li><span data-ttu-id="ce4db-128">Internet Explorer faiblement couplé</span><span class="sxs-lookup"><span data-stu-id="ce4db-128">Loosely coupled Internet Explorer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ce4db-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce4db-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce4db-130">Problèmes de compatibilité des applications lors de la migration vers Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="ce4db-130">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



