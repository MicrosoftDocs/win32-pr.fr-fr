---
description: Les énumérations ont tendance à utiliser une quantité importante de ressources système.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Amélioration des performances d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203961"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="ca1f8-103">Amélioration des performances d’énumération</span><span class="sxs-lookup"><span data-stu-id="ca1f8-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="ca1f8-104">Les énumérations ont tendance à utiliser une quantité importante de ressources système.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="ca1f8-105">Par conséquent, vous devez essayer d’optimiser le processus d’énumération WMI si vous envisagez d’effectuer des énumérations sur un grand groupe.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="ca1f8-106">Les scripts peuvent également utiliser une requête pour éviter une dégradation des performances dans les opérations « for each.... Next » avec un grand ensemble.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="ca1f8-107">Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ca1f8-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="ca1f8-108">La procédure suivante décrit comment améliorer les performances de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="ca1f8-109">**Pour améliorer les performances de l’énumération**</span><span class="sxs-lookup"><span data-stu-id="ca1f8-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="ca1f8-110">Définissez le paramètre *lFlags* pour autoriser le retour semi-synchrone des données avec un énumérateur qui ignore chaque élément de WMI lorsqu’il est remis.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="ca1f8-111">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca1f8-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="ca1f8-112">L’exemple de code C++ suivant montre comment utiliser l' **indicateur WBEM pour \_ \_ retourner \_** les indicateurs de transfert immédiat et de l' **\_ indicateur WBEM \_ Forward \_ uniquement** .</span><span class="sxs-lookup"><span data-stu-id="ca1f8-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="ca1f8-113">Dans VBScript ou Visual Basic, utilisez les indicateurs de script **WbemFlagReturnImmediately** et **WbemFlagForwardOnly** à partir de [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span><span class="sxs-lookup"><span data-stu-id="ca1f8-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="ca1f8-114">La valeur combinée de ces indicateurs est décimale 48.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="ca1f8-115">Les indicateurs de script et de paramètre provoquent le comportement suivant :</span><span class="sxs-lookup"><span data-stu-id="ca1f8-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="ca1f8-116">L' **\_ indicateur WBEM \_ retourne \_** le comportement semi-synchrone ou **wbemFlagReturnImmediately** des demandes d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="ca1f8-117">L’appel pour créer l’énumérateur est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="ca1f8-118">Vous pouvez ensuite commencer à parcourir le jeu d’objets que vous recevez.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="ca1f8-119">L’indicateur de progression de l' **\_ indicateur WBEM \_ \_ uniquement** ou **wbemFlagForwardOnly** demande un énumérateur que vous ne pouvez pas rembobiner.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="ca1f8-120">Autrement dit, WMI peut libérer un objet une fois que vous avez affiché l’objet.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="ca1f8-121">Dans les situations où l’énumération est volumineuse et l’application est très rapide, l’utilisation d’énumérateurs avant uniquement avec le traitement semi-synchrone permet à WMI de conserver beaucoup moins d’objets, ce qui augmente considérablement le temps de réponse et les performances de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="ca1f8-122">L’exemple de code VBScript suivant montre comment effectuer un appel à l’aide des indicateurs **wbemFlagReturnImmediately** et **wbemFlagForwardOnly** combinés pour obtenir une collection d’événements à partir d’un journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="ca1f8-123">Dans la mesure du possible, évitez d’utiliser [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) en C++ ou [**SWbemServices. InstancesOf**](swbemservices-instancesof.md), et utilisez à la place **ExecQuery**.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="ca1f8-124">La méthode **ExecQuery** interroge WMI à l’aide des technologies de base de données, tandis que [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) ou [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) énumère les objets WMI.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="ca1f8-125">Plus précisément, **ExecQuery** peut demander des sous-ensembles spécifiques de données que les méthodes d’énumération ne peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="ca1f8-126">Étant donné que certains fournisseurs n’ont pas de fonctionnalités d’interrogation, WMI fournit une fonctionnalité « filtre de publication » qui permet à WMI d’ignorer les instances qui ne répondent pas aux spécifications de la requête.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="ca1f8-127">Le fait qu’un fournisseur particulier tire parti de cette fonctionnalité dépend de l’auteur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="ca1f8-128">Faites des essais avec différentes requêtes pour déterminer ce qui offre les meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="ca1f8-129">Par exemple, WMI traite rarement efficacement les requêtes avec des clauses **Where** de la forme Prop1 < « x ».</span><span class="sxs-lookup"><span data-stu-id="ca1f8-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="ca1f8-130">En revanche, WMI traite normalement les requêtes de la forme KeyProp1 = "x" efficacement.</span><span class="sxs-lookup"><span data-stu-id="ca1f8-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="ca1f8-131">Pour plus d’informations, consultez la page [énumération de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ca1f8-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



