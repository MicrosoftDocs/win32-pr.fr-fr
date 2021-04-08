---
title: Interfaces de requête
description: Trois types d’interfaces ADSI peuvent être utilisés pour effectuer des recherches dans les répertoires. L’environnement de l’application et d’autres conditions peuvent indiquer l’interface utilisée.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfaces ADSI des interfaces de requête
- Requêtes ADSI, interfaces de requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839145"
---
# <a name="query-interfaces"></a><span data-ttu-id="c21e1-106">Interfaces de requête</span><span class="sxs-lookup"><span data-stu-id="c21e1-106">Query Interfaces</span></span>

<span data-ttu-id="c21e1-107">Trois types d’interfaces ADSI peuvent être utilisés pour effectuer des recherches dans les répertoires.</span><span class="sxs-lookup"><span data-stu-id="c21e1-107">Three types of ADSI interfaces can be used to perform directory searches.</span></span> <span data-ttu-id="c21e1-108">L’environnement de l’application et d’autres conditions peuvent indiquer l’interface utilisée.</span><span class="sxs-lookup"><span data-stu-id="c21e1-108">The application environment and other requirements may indicate which interface is used.</span></span>

-   <span data-ttu-id="c21e1-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="c21e1-109">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="c21e1-110">**IDirectorySearch** est une interface com de base uniquement disponible pour les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="c21e1-110">**IDirectorySearch** is a basic COM interface only available to C/C++ programmers.</span></span> <span data-ttu-id="c21e1-111">Pour plus d’informations, consultez [recherche à l’aide de l’interface IDirectorySearch](searching-with-idirectorysearch.md).</span><span class="sxs-lookup"><span data-stu-id="c21e1-111">For more information, see [Searching With the IDirectorySearch Interface](searching-with-idirectorysearch.md).</span></span>
-   <span data-ttu-id="c21e1-112">Objet.</span><span class="sxs-lookup"><span data-stu-id="c21e1-112">ADO.</span></span> <span data-ttu-id="c21e1-113">Les interfaces ADO (ActiveX Data Object) sont des interfaces d’automatisation qui utilisent OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c21e1-113">The ActiveX Data Object (ADO) interfaces are Automation interfaces that use OLE DB.</span></span> <span data-ttu-id="c21e1-114">Utilisez ADO pour les requêtes dans les applications qui reposent sur l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="c21e1-114">Use ADO for queries within applications that rely on Automation.</span></span> <span data-ttu-id="c21e1-115">Il s’agit notamment des applications Visual Basic, Active Server des pages, etc.</span><span class="sxs-lookup"><span data-stu-id="c21e1-115">These include Visual Basic applications, Active Server Pages, and so on.</span></span> <span data-ttu-id="c21e1-116">Pour plus d’informations, consultez [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c21e1-116">For more information, see [Searching with ActiveX Data Objects](searching-with-activex-data-objects-ado.md).</span></span>
-   <span data-ttu-id="c21e1-117">OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c21e1-117">OLE DB.</span></span> <span data-ttu-id="c21e1-118">OLE DB est un ensemble d’interfaces C/C++ utilisées pour interroger des bases de données.</span><span class="sxs-lookup"><span data-stu-id="c21e1-118">OLE DB is a set of C/C++ interfaces used to query databases.</span></span> <span data-ttu-id="c21e1-119">En prenant en charge ces interfaces, les fournisseurs ADSI peuvent implémenter des fonctionnalités de OLE DB avancées, telles que des requêtes distribuées avec d’autres fournisseurs de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c21e1-119">By supporting these interfaces, ADSI providers can implement advanced OLE DB features, such as distributed queries with other OLE DB providers.</span></span> <span data-ttu-id="c21e1-120">Pour plus d’informations, consultez [recherche avec OLE DB](searching-with-ole-db.md).</span><span class="sxs-lookup"><span data-stu-id="c21e1-120">For more information, see [Searching with OLE DB](searching-with-ole-db.md).</span></span>

 

 




