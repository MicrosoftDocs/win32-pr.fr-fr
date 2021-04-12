---
title: QueryType (type complexe)
description: Définit un ensemble de requêtes de sélecteur et de suppresseur utilisées pour inclure des événements dans ou exclure des événements du jeu de résultats.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- TypeRequête type complexe EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103576"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="ef22e-104">QueryType (type complexe)</span><span class="sxs-lookup"><span data-stu-id="ef22e-104">QueryType Complex Type</span></span>

<span data-ttu-id="ef22e-105">Définit un ensemble de requêtes de sélecteur et de suppresseur utilisées pour inclure des événements dans ou exclure des événements du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="ef22e-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ef22e-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ef22e-106">Child elements</span></span>



| <span data-ttu-id="ef22e-107">Élément</span><span class="sxs-lookup"><span data-stu-id="ef22e-107">Element</span></span>                                                    | <span data-ttu-id="ef22e-108">Type</span><span class="sxs-lookup"><span data-stu-id="ef22e-108">Type</span></span> | <span data-ttu-id="ef22e-109">Description</span><span class="sxs-lookup"><span data-stu-id="ef22e-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef22e-110">**Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="ef22e-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="ef22e-111">Requête XPath qui identifie les événements à inclure dans le jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="ef22e-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="ef22e-112">Spécifiez le XPath dans le corps de texte de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ef22e-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="ef22e-113">Le XPath est limité à 32 expressions.</span><span class="sxs-lookup"><span data-stu-id="ef22e-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="ef22e-114">**Suppress**</span><span class="sxs-lookup"><span data-stu-id="ef22e-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="ef22e-115">Requête XPath qui identifie les événements à exclure du jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="ef22e-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="ef22e-116">Spécifiez le XPath dans le corps de texte de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ef22e-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="ef22e-117">Le XPath est limité à 32 expressions.</span><span class="sxs-lookup"><span data-stu-id="ef22e-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="ef22e-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ef22e-118">Attributes</span></span>



| <span data-ttu-id="ef22e-119">Nom</span><span class="sxs-lookup"><span data-stu-id="ef22e-119">Name</span></span> | <span data-ttu-id="ef22e-120">Type</span><span class="sxs-lookup"><span data-stu-id="ef22e-120">Type</span></span>   | <span data-ttu-id="ef22e-121">Description</span><span class="sxs-lookup"><span data-stu-id="ef22e-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef22e-122">Id</span><span class="sxs-lookup"><span data-stu-id="ef22e-122">Id</span></span>   | <span data-ttu-id="ef22e-123">long</span><span class="sxs-lookup"><span data-stu-id="ef22e-123">long</span></span>   | <span data-ttu-id="ef22e-124">Identificateur qui identifie de façon unique cette requête dans votre liste de requêtes.</span><span class="sxs-lookup"><span data-stu-id="ef22e-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="ef22e-125">L’identificateur est de base zéro.</span><span class="sxs-lookup"><span data-stu-id="ef22e-125">The identifier is zero-based.</span></span> <span data-ttu-id="ef22e-126">Vous devez spécifier un identificateur si votre liste de requêtes contient plus d’une requête.</span><span class="sxs-lookup"><span data-stu-id="ef22e-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="ef22e-127">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ef22e-127">Path</span></span> | <span data-ttu-id="ef22e-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="ef22e-128">anyURI</span></span> | <span data-ttu-id="ef22e-129">Nom du canal ou chemin d’accès au fichier journal qui contient les événements.</span><span class="sxs-lookup"><span data-stu-id="ef22e-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="ef22e-130">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ef22e-130">Path</span></span> | <span data-ttu-id="ef22e-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="ef22e-131">anyURI</span></span> | <span data-ttu-id="ef22e-132">Nom du canal ou chemin d’accès au fichier journal qui contient les événements.</span><span class="sxs-lookup"><span data-stu-id="ef22e-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="ef22e-133">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="ef22e-133">Path</span></span> | <span data-ttu-id="ef22e-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="ef22e-134">anyURI</span></span> | <span data-ttu-id="ef22e-135">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ef22e-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="ef22e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="ef22e-136">Remarks</span></span>

<span data-ttu-id="ef22e-137">La requête doit avoir au moins une instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="ef22e-137">The query must have at least one select statement.</span></span> <span data-ttu-id="ef22e-138">Pour chaque instruction de suppression, il doit y avoir au moins une instruction SELECT qui spécifie le même chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ef22e-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="ef22e-139">Si la requête SELECT et Suppress renvoient les mêmes événements, l’instruction de suppression est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="ef22e-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="ef22e-140">Si vous sélectionnez des événements de plusieurs sources, les événements sont retournés dans l’ordre des horodatages.</span><span class="sxs-lookup"><span data-stu-id="ef22e-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="ef22e-141">Si vous utilisez l’horodatage du système et que le taux d’événements est élevé, il est possible que plusieurs événements aient le même horodatage.</span><span class="sxs-lookup"><span data-stu-id="ef22e-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="ef22e-142">Dans ce cas, l’ordre des événements devient ambigu et les événements peuvent apparaître dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="ef22e-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="ef22e-143">Si vous spécifiez un chemin d’accès pour l’une des requêtes de la liste des requêtes, toutes les requêtes doivent spécifier un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ef22e-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="ef22e-144">Si vous ne spécifiez pas de chemin d’accès pour toutes les requêtes, vous devez spécifier le chemin d’accès lors de l’appel de la fonction [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="ef22e-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef22e-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef22e-145">Requirements</span></span>



| <span data-ttu-id="ef22e-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef22e-146">Requirement</span></span> | <span data-ttu-id="ef22e-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef22e-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef22e-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef22e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ef22e-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef22e-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef22e-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef22e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ef22e-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef22e-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





