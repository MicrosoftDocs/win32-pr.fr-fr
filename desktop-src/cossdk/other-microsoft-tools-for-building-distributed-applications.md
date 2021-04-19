---
description: Autres outils Microsoft pour la création d’applications distribuées
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Autres outils Microsoft pour la création d’applications distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513947"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="7d421-103">Autres outils Microsoft pour la création d’applications distribuées</span><span class="sxs-lookup"><span data-stu-id="7d421-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="7d421-104">Outre les outils de COM+, Microsoft fournit les outils suivants pour aider le développeur à créer des applications distribuées :</span><span class="sxs-lookup"><span data-stu-id="7d421-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="7d421-105">Microsoft Data Access Components (MDAC).</span><span class="sxs-lookup"><span data-stu-id="7d421-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="7d421-106">Microsoft fournit plusieurs voies pour la récupération de données à partir d’une multitude de sources.</span><span class="sxs-lookup"><span data-stu-id="7d421-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="7d421-107">Par exemple, OLE DB offre un ensemble d’interfaces COM pour créer des composants de base de données.</span><span class="sxs-lookup"><span data-stu-id="7d421-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="7d421-108">Les interfaces sont définies de sorte que les fournisseurs de données peuvent implémenter différents niveaux de prise en charge, en fonction des fonctionnalités du magasin de données sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="7d421-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="7d421-109">Étant donné que OLE DB est basé sur COM, il peut facilement être étendu, et les extensions sont implémentées en tant que nouvelles interfaces.</span><span class="sxs-lookup"><span data-stu-id="7d421-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="7d421-110">OLE DB comprend également une interface de programmation au niveau de l’application, appelée ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="7d421-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="7d421-111">ADO expose des interfaces doubles. il peut donc facilement être utilisé à partir de langages de script, ainsi que Microsoft Visual C++, Visual Basic et d’autres outils de développement.</span><span class="sxs-lookup"><span data-stu-id="7d421-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="7d421-112">Les développeurs peuvent également choisir d’utiliser une API générique, indépendante du fournisseur, telle que l’interface de programmation d’applications (API) de Microsoft Open Database Connectivity (ODBC).</span><span class="sxs-lookup"><span data-stu-id="7d421-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="7d421-113">L’API ODBC est une interface en langage C permettant d’accéder aux données d’un SGBD à l’aide de langage SQL (SQL).</span><span class="sxs-lookup"><span data-stu-id="7d421-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="7d421-114">Un gestionnaire de pilotes ODBC fournit les composants d’interface de programmation et d’exécution pour localiser des pilotes propres au SGBD.</span><span class="sxs-lookup"><span data-stu-id="7d421-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="7d421-115">Les pilotes ODBC, généralement fournis par le fournisseur SGBD, traduisent les appels génériques du gestionnaire de pilotes ODBC en appels à la méthode d’accès aux données native.</span><span class="sxs-lookup"><span data-stu-id="7d421-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="7d421-116">Le principal avantage de l’utilisation de l’API ODBC est que vous devez apprendre une seule API pour accéder à un large éventail de SGBD.</span><span class="sxs-lookup"><span data-stu-id="7d421-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="7d421-117">Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7d421-117">Microsoft SQL Server.</span></span> <span data-ttu-id="7d421-118">En plus de fournir un système de base de données relationnelle robuste et éloquence, Microsoft SQL Server pouvez fournir une application distribuée avec le regroupement de connexions et la sécurité qui peuvent s’intégrer au modèle de sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="7d421-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="7d421-119">Intégration des transactions COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="7d421-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="7d421-120">COMTI peut être utilisé pour intégrer des systèmes centraux à des systèmes Windows, y compris des applications COM+.</span><span class="sxs-lookup"><span data-stu-id="7d421-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="7d421-121">COMTI utilise des protocoles de communication standard (par exemple, LU 6,2) pour la communication entre les ordinateurs Windows et les ordinateurs centraux et les mini-ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7d421-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d421-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7d421-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d421-123">Hypothèses et principes de conception de COM+</span><span class="sxs-lookup"><span data-stu-id="7d421-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="7d421-124">Conception de l’application COM+ à l’aide d’UML</span><span class="sxs-lookup"><span data-stu-id="7d421-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="7d421-125">Conseils de conception générale pour l’utilisation de COM+</span><span class="sxs-lookup"><span data-stu-id="7d421-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="7d421-126">Optimisation des interactions avec le niveau de logique métier COM+</span><span class="sxs-lookup"><span data-stu-id="7d421-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



