---
description: Le kit de développement logiciel (SDK) Windows Search fournit un assembly d’interopérabilité pour que vous utilisiez des objets COM (Component Object Model) exposés par Windows Search et d’autres programmes sur les interfaces et les classes utilisant du code managé.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Utilisation de code managé avec Shell Data et Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112491"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="d5239-103">Utilisation de code managé avec Shell Data et Windows Search</span><span class="sxs-lookup"><span data-stu-id="d5239-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="d5239-104">Le kit de développement logiciel (SDK) Windows Search fournit un assembly d’interopérabilité pour que vous utilisiez des objets COM (Component Object Model) exposés par Windows Search et d’autres programmes sur les interfaces et les classes utilisant du code managé.</span><span class="sxs-lookup"><span data-stu-id="d5239-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="d5239-105">L’assembly d’interopérabilité est signé numériquement par Microsoft et se trouve dans les [exemples de recherche Windows](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="d5239-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="d5239-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="d5239-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="d5239-107">Utilisation de l’API Windows CodePack</span><span class="sxs-lookup"><span data-stu-id="d5239-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="d5239-108">Accès aux résultats de l’index</span><span class="sxs-lookup"><span data-stu-id="d5239-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="d5239-109">Exemple d’application utilisant l’API Windows Codepack</span><span class="sxs-lookup"><span data-stu-id="d5239-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="d5239-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5239-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="d5239-111">Utilisation de l’API Windows CodePack</span><span class="sxs-lookup"><span data-stu-id="d5239-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="d5239-112">Si vous travaillez dans l’environnement Microsoft .NET, utilisez le [Pack de code d’API Windows pour Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) pour obtenir des résultats de recherche, ou simplement parcourir l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d5239-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="d5239-113">Le [Pack de code d’API Windows pour Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) vous fournit une collection d’éléments de Shell qui sont essentiellement des wrappers autour de l' [interface IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)native.</span><span class="sxs-lookup"><span data-stu-id="d5239-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="d5239-114">Vous pouvez effectuer une itération sur cette collection et obtenir les différentes valeurs de propriété d’une manière similaire à la façon dont vous pouvez énumérer les résultats d’une table à partir d’une requête de base de données (OLE DB) de liaison et d’incorporation d’objets.</span><span class="sxs-lookup"><span data-stu-id="d5239-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="d5239-115">L’extrait de code suivant montre comment itérer au sein des éléments de recherche et obtenir les valeurs de propriété pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="d5239-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="d5239-116">Accès aux résultats de l’index</span><span class="sxs-lookup"><span data-stu-id="d5239-116">Accessing Index Results</span></span>

<span data-ttu-id="d5239-117">Vous pouvez accéder aux résultats de l’index par le biais de OLE DB ou du modèle de données Shell.</span><span class="sxs-lookup"><span data-stu-id="d5239-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="d5239-118">Les deux approches présentent des avantages et des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="d5239-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="d5239-119">L’un des avantages est que OLE DB et langage SQL (SQL) sont familiers aux programmeurs de base de données.</span><span class="sxs-lookup"><span data-stu-id="d5239-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="d5239-120">D’autres avantages sont un meilleur contrôle des performances lors de l’interrogation de l’indexeur, et l’accès à des fonctionnalités supplémentaires telles que la possibilité de localiser rapidement les résultats précédents dans un nouvel ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="d5239-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="d5239-121">L’avantage du modèle de données Shell est qu’il est abstrait sur différentes sources d’informations, telles que OpenSearch, et permet d’accéder à des fonctionnalités supplémentaires telles que des miniatures et des gestionnaires de propriétés.</span><span class="sxs-lookup"><span data-stu-id="d5239-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="d5239-122">Le modèle d’objet Shell ne nécessite pas non plus de prise en charge de cas spéciaux pour les résultats autres que les noms de fichiers tels que les éléments de messagerie et les résultats OneNote, ni pour les éléments qui se trouvent dans l’index de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5239-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="d5239-123">Notez que dans l’interpréteur de commandes [KNOWNFOLDERID](../shell/knownfolderid.md) est l’étendue du dossier connu pour le contenu indexé local.</span><span class="sxs-lookup"><span data-stu-id="d5239-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="d5239-124">Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d5239-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="d5239-125">Les sources de données OpenSearch ne sont pas exposées via OLE DB pour la recherche fédérée dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d5239-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="d5239-126">Pour cette raison, nous vous recommandons d’envisager d’écrire un fournisseur LINQ pour l’espace de noms Shell au lieu d’utiliser OLE DB pour accéder aux résultats de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="d5239-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="d5239-127">Pour plus d’informations, consultez [procédure pas à pas : création d’un fournisseur LINQ IQueryable](/previous-versions/bb546158(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="d5239-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="d5239-128">Exemple d’application utilisant l’API Windows Codepack</span><span class="sxs-lookup"><span data-stu-id="d5239-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="d5239-129">La capture d’écran suivante représente une simulation d’un exemple d’application créé avec le [Pack de code d’API Windows pour Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span><span class="sxs-lookup"><span data-stu-id="d5239-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![capture d’écran de l’application de lecteur multimédia montrant les messages électroniques](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="d5239-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5239-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d5239-132">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d5239-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d5239-133">Recherche fédérée dans Windows</span><span class="sxs-lookup"><span data-stu-id="d5239-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="d5239-134">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="d5239-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d5239-135">[Interopérabilité interlangage](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="d5239-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
