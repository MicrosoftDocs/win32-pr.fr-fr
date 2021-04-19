---
description: L’un des principaux outils de Windows Management Instrumentation (WMI) est la capacité à interroger le référentiel WMI pour obtenir des informations sur les classes et les instances.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Interrogation de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534170"
---
# <a name="querying-wmi"></a><span data-ttu-id="22a3c-103">Interrogation de WMI</span><span class="sxs-lookup"><span data-stu-id="22a3c-103">Querying WMI</span></span>

<span data-ttu-id="22a3c-104">L’un des principaux outils de Windows Management Instrumentation (WMI) est la capacité à interroger le référentiel WMI pour obtenir des informations sur les classes et les instances.</span><span class="sxs-lookup"><span data-stu-id="22a3c-104">One of the main tools of Windows Management Instrumentation (WMI) is the ability to query the WMI repository for class and instance information.</span></span> <span data-ttu-id="22a3c-105">Par exemple, vous pouvez demander que WMI retourne tous les objets représentant les événements d’arrêt à partir de votre système de bureau.</span><span class="sxs-lookup"><span data-stu-id="22a3c-105">For example, you can request that WMI return all the objects representing shut-down events from your desktop system.</span></span> <span data-ttu-id="22a3c-106">Vous pouvez également récupérer des données de classe, d’instance ou de schéma.</span><span class="sxs-lookup"><span data-stu-id="22a3c-106">You can also retrieve class, instance, or schema data.</span></span> <span data-ttu-id="22a3c-107">Le tableau suivant répertorie les différents types de requêtes que vous pouvez effectuer.</span><span class="sxs-lookup"><span data-stu-id="22a3c-107">The following table lists the different types of queries you can make.</span></span>



| <span data-ttu-id="22a3c-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="22a3c-108">Topic</span></span>                                                                | <span data-ttu-id="22a3c-109">Description</span><span class="sxs-lookup"><span data-stu-id="22a3c-109">Description</span></span>                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22a3c-110">Appel d’une requête synchrone</span><span class="sxs-lookup"><span data-stu-id="22a3c-110">Invoking a Synchronous Query</span></span>](invoking-a-synchronous-query.md)     | <span data-ttu-id="22a3c-111">Décrit comment conserver un lien avec WMI tout au long du processus de requête.</span><span class="sxs-lookup"><span data-stu-id="22a3c-111">Describes how to maintain a link with WMI throughout the query process.</span></span> <span data-ttu-id="22a3c-112">Les requêtes synchrones sont efficaces pour les requêtes ou les requêtes de petite taille sur un système local.</span><span class="sxs-lookup"><span data-stu-id="22a3c-112">Synchronous queries are good for small queries or queries to a local system.</span></span><br/>                                  |
| [<span data-ttu-id="22a3c-113">Appel d’une requête asynchrone</span><span class="sxs-lookup"><span data-stu-id="22a3c-113">Invoking an Asynchronous Query</span></span>](invoking-an-asynchronous-query.md) | <span data-ttu-id="22a3c-114">Décrit comment configurer un processus distinct pour recevoir des requêtes.</span><span class="sxs-lookup"><span data-stu-id="22a3c-114">Describes how to set up a separate process to receive queries.</span></span> <span data-ttu-id="22a3c-115">Les requêtes asynchrones sont plus complexes et offrent un niveau de sécurité inférieur, mais améliorent généralement les performances du système.</span><span class="sxs-lookup"><span data-stu-id="22a3c-115">Asynchronous queries are more complex and provide a lower level of security, but generally improve system performance.</span></span><br/> |



 

<span data-ttu-id="22a3c-116">Outre l’interrogation de l’espace de stockage WMI, vous pouvez également utiliser le [*langage de requêtes WMI (WQL) (WQL)*](gloss-w.md) pour acheminer les événements de notification vers votre application.</span><span class="sxs-lookup"><span data-stu-id="22a3c-116">In addition to querying the WMI repository, you can also use the [*WMI Query Language (WQL)*](gloss-w.md) to route notification events to your application.</span></span> <span data-ttu-id="22a3c-117">Pour plus d’informations, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="22a3c-117">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

> [!Note]
>
> <span data-ttu-id="22a3c-118">Pour interroger correctement WMI, vous devez avoir une bonne compréhension de WQL.</span><span class="sxs-lookup"><span data-stu-id="22a3c-118">To properly query WMI, you must have a good understanding of WQL.</span></span> <span data-ttu-id="22a3c-119">Une requête incorrecte, trop complexe ou inappropriée peut entraîner le retour d’une erreur ou des résultats inattendus par le processeur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="22a3c-119">A query that is incorrect, too complex, or inappropriate can cause the query processor to return an error or unexpected results.</span></span> <span data-ttu-id="22a3c-120">Pour obtenir un guide complet sur WQL, consultez [interrogation avec WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="22a3c-120">For a comprehensive guide to WQL, see [Querying with WQL](querying-with-wql.md).</span></span>
>
> <span data-ttu-id="22a3c-121">Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="22a3c-121">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="22a3c-122">Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de  **\_ \_ \_ violation de quota E WBEM** en tant que valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="22a3c-122">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="22a3c-123">La limite des mots clés WQL dépend de la complexité de la requête.</span><span class="sxs-lookup"><span data-stu-id="22a3c-123">The limit of WQL keywords depends on how complex the query is.</span></span>
>
> <span data-ttu-id="22a3c-124">Lors de l’interrogation des valeurs de propriété avec un type de données **UInt64** ou **sint64** dans un langage de script tel que VBScript, WMI retourne des valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="22a3c-124">When querying for property values with a **uint64** or **sint64** data type in a scripting language like VBScript, WMI returns string values.</span></span> <span data-ttu-id="22a3c-125">Des résultats inattendus peuvent se produire lors de la comparaison de ces valeurs, car la comparaison de chaînes retourne différents résultats que la comparaison de nombres.</span><span class="sxs-lookup"><span data-stu-id="22a3c-125">Unexpected results can occur when comparing these values, because comparing strings returns different results than comparing numbers.</span></span> <span data-ttu-id="22a3c-126">Par exemple, « 10 milliards » est inférieur à « 9 » lors de la comparaison de chaînes et 9 est inférieur à 10 milliards lors de la comparaison de nombres.</span><span class="sxs-lookup"><span data-stu-id="22a3c-126">For example, "10000000000" is less than "9" when comparing strings, and 9 is less than 10000000000 when comparing numbers.</span></span> <span data-ttu-id="22a3c-127">Pour éviter toute confusion, vous devez utiliser la méthode [CDbl](/previous-versions//ftekwwt0(v=vs.85)) dans VBScript lorsque les propriétés de type **UInt64** ou **sint64** sont récupérées à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="22a3c-127">To avoid confusion you should use the [CDbl](/previous-versions//ftekwwt0(v=vs.85)) method in VBScript when properties of type **uint64** or **sint64** are retrieved from WMI.</span></span>

 

> [!Note]  

 

<span data-ttu-id="22a3c-128">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="22a3c-128">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

