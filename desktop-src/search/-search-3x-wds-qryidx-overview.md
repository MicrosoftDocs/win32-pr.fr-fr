---
description: Il existe plusieurs façons d’utiliser Windows Search pour interroger l’index.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Interrogation de l’index programmatiquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536324"
---
# <a name="querying-the-index-programmatically"></a><span data-ttu-id="d1519-103">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="d1519-103">Querying the Index Programmatically</span></span>

<span data-ttu-id="d1519-104">Il existe plusieurs façons d’utiliser Windows Search pour interroger l’index.</span><span class="sxs-lookup"><span data-stu-id="d1519-104">There are several ways to use Windows Search to query the index.</span></span>

<span data-ttu-id="d1519-105">Cette section fournit l’infrastructure conceptuelle pour l’interrogation de l’index par programme :</span><span class="sxs-lookup"><span data-stu-id="d1519-105">This section provides the conceptual framework for querying the index programmatically:</span></span>

-   [<span data-ttu-id="d1519-106">Utilisation des approches SQL et AQS pour interroger l’index</span><span class="sxs-lookup"><span data-stu-id="d1519-106">Using SQL and AQS Approaches to Query the Index</span></span>](using-sql-and-aqs-to-query-the-index.md)
-   [<span data-ttu-id="d1519-107">Interrogation de l’index avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="d1519-107">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [<span data-ttu-id="d1519-108">Interrogation de l’index avec le protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="d1519-108">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
-   [<span data-ttu-id="d1519-109">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="d1519-109">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
-   [<span data-ttu-id="d1519-110">Utilisation de la syntaxe de requête avancée par programmation</span><span class="sxs-lookup"><span data-stu-id="d1519-110">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)

> [!Note]  
> <span data-ttu-id="d1519-111">Compatibilité héritée de Microsoft Windows Desktop Search (WDS) 2x : sur les ordinateurs exécutant Windows XP et versions ultérieures, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="d1519-111">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="d1519-112">Au lieu de cela, les développeurs doivent utiliser [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) pour obtenir une chaîne de connexion et analyser la requête de l’utilisateur dans langage SQL (SQL), puis interroger la base de données de liaison et d’incorporation d’objets (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="d1519-112">Instead, developers should use [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string and to parse the user's query into Structured Query Language (SQL), and then query through Object Linking and Embedding Database (OLE DB).</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="d1519-113">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="d1519-113">Additional Resources</span></span>

-   <span data-ttu-id="d1519-114">Pour plus d’informations sur la OLE DB, consultez [OLE DB vue d’ensemble](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx)de la programmation.</span><span class="sxs-lookup"><span data-stu-id="d1519-114">For information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx).</span></span> <span data-ttu-id="d1519-115">Pour plus d’informations sur le Fournisseur de données .NET Framework pour OLE DB, consultez l' [espace de noms System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span><span class="sxs-lookup"><span data-stu-id="d1519-115">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).</span></span>
-   <span data-ttu-id="d1519-116">Pour plus d’informations sur l’utilisation des propriétés dans l’interrogation, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1519-116">For additional background on using properties in querying, see the following topics:</span></span>
    -   [<span data-ttu-id="d1519-117">Système de propriétés</span><span class="sxs-lookup"><span data-stu-id="d1519-117">Property System</span></span>](../properties/building-property-handlers.md)
    -   <span data-ttu-id="d1519-118">[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d1519-118">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
-   <span data-ttu-id="d1519-119">Pour plus d’informations sur la façon de créer et de modifier des dossiers de recherche, consultez [**ISearchFolderItemFactory interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span><span class="sxs-lookup"><span data-stu-id="d1519-119">For information on how to create and modify search folders, see [**ISearchFolderItemFactory Interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).</span></span>
-   <span data-ttu-id="d1519-120">Pour obtenir des forums de discussion et des questions sur les technologies de recherche prises en charge par la Communauté, consultez le [forum MSDN : développement de Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="d1519-120">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
-   <span data-ttu-id="d1519-121">Pour télécharger les exemples de code du kit de développement logiciel (SDK) Search :</span><span class="sxs-lookup"><span data-stu-id="d1519-121">To download the Search SDK Code Samples:</span></span>
    -   <span data-ttu-id="d1519-122">Pour Windows 7 : [exemples de recherche Windows sur GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span><span class="sxs-lookup"><span data-stu-id="d1519-122">For Windows 7: [Windows Search Samples on GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)</span></span>
    -   <span data-ttu-id="d1519-123">Pour Windows Vista : [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span><span class="sxs-lookup"><span data-stu-id="d1519-123">For Windows Vista: [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)</span></span>
-   <span data-ttu-id="d1519-124">Pour télécharger les SDK Windows :</span><span class="sxs-lookup"><span data-stu-id="d1519-124">To download the Windows SDK:</span></span>
    -   <span data-ttu-id="d1519-125">Pour Windows 7 : [SDK Windows pour Windows 7 et .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1519-125">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>
    -   <span data-ttu-id="d1519-126">Pour Windows Vista : [SDK Windows pour Windows Vista et .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span><span class="sxs-lookup"><span data-stu-id="d1519-126">For Windows Vista: [Windows SDK for Windows Vista and .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1519-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1519-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1519-128">Guide de développement de Windows Search</span><span class="sxs-lookup"><span data-stu-id="d1519-128">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="d1519-129">Gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="d1519-129">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="d1519-130">Extension de l’index de recherche Windows</span><span class="sxs-lookup"><span data-stu-id="d1519-130">Extending the Windows Search Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[<span data-ttu-id="d1519-131">Extension des ressources linguistiques</span><span class="sxs-lookup"><span data-stu-id="d1519-131">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
