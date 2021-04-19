---
description: Le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble de American National Standards Institute standard langage SQL (ANSI SQL) avec des modifications sémantiques mineures pour prendre en charge WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Interrogation avec WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534171"
---
# <a name="querying-with-wql"></a><span data-ttu-id="dee16-103">Interrogation avec WQL</span><span class="sxs-lookup"><span data-stu-id="dee16-103">Querying with WQL</span></span>

<span data-ttu-id="dee16-104">Le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble de American National Standards Institute standard langage SQL (ANSI SQL) avec des modifications sémantiques mineures pour prendre en charge WMI.</span><span class="sxs-lookup"><span data-stu-id="dee16-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="dee16-105">Pour obtenir la liste complète des mots clés WQL pris en charge, consultez [WQL (SQL pour WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="dee16-106">L’utilisation de mots clés SQL pour les noms d’objets ou de propriétés peut empêcher l’analyse d’une requête.</span><span class="sxs-lookup"><span data-stu-id="dee16-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="dee16-107">Les mots clés SQL suivants sont restreints : **null**, **true** et **false**.</span><span class="sxs-lookup"><span data-stu-id="dee16-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="dee16-108">Il existe des limites concernant le nombre de mots clés AND et OR qui peuvent être utilisés dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="dee16-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="dee16-109">Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de  **\_ \_ \_ violation de quota E WBEM** en tant que valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="dee16-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="dee16-110">La limite des mots clés WQL dépend de la complexité de la requête.</span><span class="sxs-lookup"><span data-stu-id="dee16-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="dee16-111">Les requêtes peuvent utiliser la clause **Where** pour l’extension et la personnalisation, bien que cela ne soit pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dee16-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="dee16-112">La clause **Where** est constituée d’une propriété ou d’un mot clé, d’un opérateur et d’une constante.</span><span class="sxs-lookup"><span data-stu-id="dee16-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="dee16-113">Toutes les clauses **Where** doivent spécifier l’un des opérateurs prédéfinis qui sont inclus dans WQL.</span><span class="sxs-lookup"><span data-stu-id="dee16-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="dee16-114">Pour plus d’informations sur la syntaxe, consultez [Where, clause](where-clause.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="dee16-115">Pour plus d’informations sur les opérateurs WQL valides, consultez [opérateurs WQL](wql-operators.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="dee16-116">Comme avec d’autres chaînes de requête SQL, vous pouvez échapper vos requêtes.</span><span class="sxs-lookup"><span data-stu-id="dee16-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="dee16-117">WQL ne prend pas en charge les requêtes ou les associations entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="dee16-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="dee16-118">Vous ne pouvez pas interroger toutes les instances d’une classe spécifiée résidant dans tous les espaces de noms sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="dee16-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="dee16-119">WQL prend en charge les types de requêtes suivants :</span><span class="sxs-lookup"><span data-stu-id="dee16-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="dee16-120">Requêtes de données</span><span class="sxs-lookup"><span data-stu-id="dee16-120">Data queries</span></span>

    <span data-ttu-id="dee16-121">Les requêtes de données sont utilisées pour récupérer des instances de classe et des associations de données.</span><span class="sxs-lookup"><span data-stu-id="dee16-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="dee16-122">Il s’agit du type de requête le plus couramment utilisé dans les applications et les scripts WMI.</span><span class="sxs-lookup"><span data-stu-id="dee16-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="dee16-123">Pour plus d’informations sur la syntaxe des requêtes de données, consultez [demande de données d’instance de classe](requesting-class-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="dee16-124">Pour plus d’informations sur les associations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="dee16-125">WQL ne prend pas en charge les requêtes de types de données de tableau.</span><span class="sxs-lookup"><span data-stu-id="dee16-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="dee16-126">L’exemple de requête de données suivant demande le fichier journal des événements nommé « application » à partir de toutes les instances de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="dee16-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="dee16-127">Requêtes d’événements</span><span class="sxs-lookup"><span data-stu-id="dee16-127">Event queries</span></span>

    <span data-ttu-id="dee16-128">Les consommateurs utilisent des requêtes d’événements pour s’inscrire afin de recevoir des notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="dee16-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="dee16-129">Les fournisseurs d’événements utilisent des requêtes d’événement pour s’inscrire afin de prendre en charge un ou plusieurs événements.</span><span class="sxs-lookup"><span data-stu-id="dee16-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="dee16-130">Pour plus d’informations sur les requêtes d’événements, consultez [réception de notifications d’événements](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="dee16-131">L’exemple suivant de requête d’événement par un consommateur d’événements temporaire demande une notification lorsqu’une nouvelle instance d’une classe dérivée de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) est créée.</span><span class="sxs-lookup"><span data-stu-id="dee16-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="dee16-132">Requêtes de schéma</span><span class="sxs-lookup"><span data-stu-id="dee16-132">Schema queries</span></span>

    <span data-ttu-id="dee16-133">Les requêtes de schéma sont utilisées pour récupérer les définitions de classe (plutôt que les instances de classe) et les associations de schéma.</span><span class="sxs-lookup"><span data-stu-id="dee16-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="dee16-134">Les fournisseurs de classes utilisent des requêtes de schéma pour spécifier les classes qu’ils prennent en charge lorsqu’ils s’inscrivent.</span><span class="sxs-lookup"><span data-stu-id="dee16-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="dee16-135">Pour plus d’informations sur les requêtes de schéma, consultez [extraction de définitions de classe](retrieving-class-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="dee16-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="dee16-136">L’exemple de requête de schéma suivant montre la syntaxe spéciale.</span><span class="sxs-lookup"><span data-stu-id="dee16-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="dee16-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dee16-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dee16-138">Format de date et d’heure WMI</span><span class="sxs-lookup"><span data-stu-id="dee16-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
