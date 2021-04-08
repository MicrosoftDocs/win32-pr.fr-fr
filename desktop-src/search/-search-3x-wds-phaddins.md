---
description: Cette section fournit des informations conceptuelles nécessaires à l’implémentation, l’extension et le test des gestionnaires de protocole.
ms.assetid: c76d5c82-d62b-4dd4-9743-9572be61e2be
title: Développement de gestionnaires de protocole pour Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e56c237dd4876ae05bcd7b983c4da2708f299a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750428"
---
# <a name="developing-protocol-handlers-for-windows-search"></a><span data-ttu-id="6630e-103">Développement de gestionnaires de protocole pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="6630e-103">Developing Protocol Handlers for Windows Search</span></span>

<span data-ttu-id="6630e-104">Cette section fournit des informations conceptuelles nécessaires à l’implémentation, l’extension et le test des gestionnaires de protocole.</span><span class="sxs-lookup"><span data-stu-id="6630e-104">This section provides conceptual information necessary for the implementation, extension and testing of protocol handlers.</span></span>

-   [<span data-ttu-id="6630e-105">Fonctionnement des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6630e-105">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
-   [<span data-ttu-id="6630e-106">Notification de l’index des modifications</span><span class="sxs-lookup"><span data-stu-id="6630e-106">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
-   [<span data-ttu-id="6630e-107">Ajout d’icônes et de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="6630e-107">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
-   [<span data-ttu-id="6630e-108">Exemple de code : extensions de Shell pour les gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6630e-108">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
-   [<span data-ttu-id="6630e-109">Installation et inscription de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6630e-109">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
-   [<span data-ttu-id="6630e-110">Création d’un connecteur de recherche pour un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="6630e-110">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
-   [<span data-ttu-id="6630e-111">Débogage de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="6630e-111">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)

## <a name="additional-resources"></a><span data-ttu-id="6630e-112">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6630e-112">Additional Resources</span></span>

<span data-ttu-id="6630e-113">Pour obtenir des informations conceptuelles sur l’indexation, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6630e-113">For conceptual background on indexing, see the following topics:</span></span>

-   <span data-ttu-id="6630e-114">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6630e-114">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="6630e-115">Pour étendre Windows Search afin d’indexer le contenu et les propriétés de nouveaux formats de fichier et de magasins de données, consultez [extension de l’index](-search-3x-wds-extidx-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6630e-115">To extend Windows Search to index the contents and properties of new file formats and data stores, see [Extending the Index](-search-3x-wds-extidx-overview.md).</span></span>
-   <span data-ttu-id="6630e-116">Pour obtenir une vue d’ensemble du gestionnaire de catalogues et du gestionnaire de recherche de catalogue (CSM), consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="6630e-116">For overviews of the Catalog Manager and Catalog Search Manager (CSM), see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

<span data-ttu-id="6630e-117">Pour obtenir des informations conceptuelles conceptuelles sur les types de fichiers et les gestionnaires, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6630e-117">For conceptual background on file types and handlers, see the following topics:</span></span>

-   <span data-ttu-id="6630e-118">Pour étendre l’interpréteur de commandes avec des gestionnaires de types de fichiers, consultez [création de gestionnaires d’extension de Shell](../shell/handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6630e-118">To extend the Shell with file type handlers, see [Creating Shell Extension Handlers](../shell/handlers.md).</span></span>
-   <span data-ttu-id="6630e-119">Pour obtenir des informations conceptuelles sur les gestionnaires de filtres, consultez [développement de gestionnaires de filtres](-search-ifilter-conceptual.md).</span><span class="sxs-lookup"><span data-stu-id="6630e-119">For conceptual information on filter handlers, see [Developing Filter Handlers](-search-ifilter-conceptual.md).</span></span>
-   <span data-ttu-id="6630e-120">Pour plus d’informations sur la création de gestionnaires, consultez [Introduction aux associations de fichiers](../shell/fa-intro.md), [inscription d’extensions de Shell](../shell/reg-shell-exts.md), création de gestionnaires d’extensions de [Shell](../shell/handlers.md), [menu contextuel](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))et [gestionnaires d’aperçus](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6630e-120">For information about creating handlers, see [Introduction to File Associations](../shell/fa-intro.md), [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), and [Preview Handlers](../shell/preview-handlers.md).</span></span>

<span data-ttu-id="6630e-121">Pour plus d’informations sur les technologies associées et sur l’implémentation d’un magasin de données, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6630e-121">For background on related technologies and on implementing a data store, see the following topics:</span></span>

-   <span data-ttu-id="6630e-122">Les gestionnaires de protocoles de recherche Windows utilisent des spécifications de conception similaires à celles de SharePoint Server, et ils peuvent souvent être utilisés de manière interchangeable.</span><span class="sxs-lookup"><span data-stu-id="6630e-122">Windows Search protocol handlers use design specifications similar to SharePoint Server, and they can often be used interchangeably.</span></span> <span data-ttu-id="6630e-123">Pour plus d’informations, consultez le [Centre de développement SharePoint Server](https://developer.microsoft.com/office/docs).</span><span class="sxs-lookup"><span data-stu-id="6630e-123">For more information, see [SharePoint Server Developer Center](https://developer.microsoft.com/office/docs).</span></span>
-   <span data-ttu-id="6630e-124">Dans Windows 7 et versions ultérieures, SharePoint Search Server 2008 et MOSS 2007 SP2 prennent également en charge la recherche fédérée.</span><span class="sxs-lookup"><span data-stu-id="6630e-124">In Windows 7 and later, SharePoint Search Server 2008 and MOSS 2007 SP2 also support federated search.</span></span> <span data-ttu-id="6630e-125">Pour plus d’informations sur le déploiement de la recherche fédérée et du serveur de recherche 2008 avec Office SharePoint Server 2007, voir serveur de recherche de recherche [fédéré \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)).</span><span class="sxs-lookup"><span data-stu-id="6630e-125">For more information about federated search and Search Server 2008 deployment with Office SharePoint Server 2007, see [Federated Search \[Search Server 2008\]](/previous-versions/office/bb931109(v=office.14)).</span></span>
-   <span data-ttu-id="6630e-126">Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6630e-126">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="6630e-127">Pour obtenir des exemples de code, consultez les pages suivantes du portail :</span><span class="sxs-lookup"><span data-stu-id="6630e-127">For code samples, see the following portal pages:</span></span>

-   <span data-ttu-id="6630e-128">Pour obtenir des exemples de code de recherche, consultez les [exemples du kit de développement Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="6630e-128">For Search code samples, see [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>
-   <span data-ttu-id="6630e-129">Pour obtenir des exemples de code Shell, consultez [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6630e-129">For Shell code samples, see [Shell SDK Samples](/previous-versions/windows/desktop/legacy/dd940376(v=vs.85)).</span></span>

 

 
