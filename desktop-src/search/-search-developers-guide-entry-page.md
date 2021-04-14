---
description: Des tiers peuvent créer des applications qui interrogent l’index sur les données par programme et peuvent étendre Windows Search pour indexer les données des formats de fichiers personnalisés et des magasins de données.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guide du développeur Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484441"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="9bc23-103">Guide du développeur Windows Search</span><span class="sxs-lookup"><span data-stu-id="9bc23-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="9bc23-104">Des tiers peuvent créer des applications qui interrogent l’index sur les données par programme et peuvent étendre Windows Search pour indexer les données des formats de fichiers personnalisés et des magasins de données.</span><span class="sxs-lookup"><span data-stu-id="9bc23-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="9bc23-105">Pour créer des applications de recherche Windows, les développeurs tiers doivent tout d’abord implémenter un magasin de données Shell pour obtenir une expérience utilisateur raisonnable.</span><span class="sxs-lookup"><span data-stu-id="9bc23-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="9bc23-106">Pour plus d’informations, consultez [implémentation des interfaces d’objets de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9bc23-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="9bc23-107">Vous devez également télécharger le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour les bibliothèques de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="9bc23-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="9bc23-108">Les [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contiennent des exemples de code utiles et un assembly d’interopérabilité pour le développement avec du code managé.</span><span class="sxs-lookup"><span data-stu-id="9bc23-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="9bc23-109">Pour plus d’informations sur l’utilisation des exemples de code, consultez [exemples de code Windows Search](-search-3x-wds-sampleentry.md).</span><span class="sxs-lookup"><span data-stu-id="9bc23-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="9bc23-110">Cette section est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="9bc23-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="9bc23-111">Gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="9bc23-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="9bc23-112">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="9bc23-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="9bc23-113">Extension de l’index</span><span class="sxs-lookup"><span data-stu-id="9bc23-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="9bc23-114">Extension des ressources linguistiques</span><span class="sxs-lookup"><span data-stu-id="9bc23-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="9bc23-115">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9bc23-115">Additional Resources</span></span>

- <span data-ttu-id="9bc23-116">Pour obtenir des forums de discussion et des questions sur les technologies de recherche prises en charge par la Communauté, consultez le [forum MSDN : développement de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="9bc23-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="9bc23-117">Pour télécharger les exemples de code de recherche :</span><span class="sxs-lookup"><span data-stu-id="9bc23-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="9bc23-118">Exemples de recherche Windows</span><span class="sxs-lookup"><span data-stu-id="9bc23-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="9bc23-119">Pour télécharger les SDK Windows :</span><span class="sxs-lookup"><span data-stu-id="9bc23-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="9bc23-120">Pour Windows 10 : [SDK Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="9bc23-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="9bc23-121">Pour Windows 7 : [SDK Windows pour Windows 7 et .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="9bc23-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bc23-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bc23-122">Related topics</span></span>

[<span data-ttu-id="9bc23-123">Vue d’ensemble de Windows Search</span><span class="sxs-lookup"><span data-stu-id="9bc23-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="9bc23-124">Référence de recherche Windows</span><span class="sxs-lookup"><span data-stu-id="9bc23-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="9bc23-125">Exemples de code Windows Search</span><span class="sxs-lookup"><span data-stu-id="9bc23-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="9bc23-126">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="9bc23-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="9bc23-127">Technologies de recherche associées</span><span class="sxs-lookup"><span data-stu-id="9bc23-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="9bc23-128">Glossaire Windows Search</span><span class="sxs-lookup"><span data-stu-id="9bc23-128">Windows Search Glossary</span></span>](search-glossary.md)
