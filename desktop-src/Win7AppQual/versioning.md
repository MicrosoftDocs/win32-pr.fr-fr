---
description: Contrôle de version (Windows 7 et Windows Server 2008 R2-conseils de qualité des applications)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Contrôle de version (Windows 7 et Windows Server 2008 R2-conseils de qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c3bc1f63dc236c706fd8d9bd6a6053371dd363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103697"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="31ae3-103">Contrôle de version (Windows 7 et Windows Server 2008 R2-conseils de qualité des applications)</span><span class="sxs-lookup"><span data-stu-id="31ae3-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="31ae3-104">L’un des problèmes les plus courants de compatibilité des applications pour Windows Internet Explorer est l’agent utilisateur (UA), les chaînes et les vecteurs de version.</span><span class="sxs-lookup"><span data-stu-id="31ae3-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="31ae3-105">Windows Internet Explorer 8 introduit une nouvelle chaîne UA pour aider les applications à détecter la version exécutée par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="31ae3-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="31ae3-106">En plus d’améliorer simplement la valeur MSIE associée à Internet Explorer dans la chaîne UA, Internet Explorer 8 ajoute une valeur Trident/4.0 pour vous aider à détecter si Internet Explorer 8 s’exécute en mode d’affichage de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="31ae3-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="31ae3-107">Ces modifications, ainsi que les vérifications de version codées en dur, peuvent potentiellement introduire des problèmes de compatibilité entre les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="31ae3-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31ae3-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31ae3-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31ae3-109">Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="31ae3-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



