---
title: Élément Value (namedValues)
description: Contient la valeur associée à un nom dans une paire nom-valeur.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Élément Value Planificateur de tâches
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743317"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="fa86e-104">Élément Value (namedValues)</span><span class="sxs-lookup"><span data-stu-id="fa86e-104">Value (namedValues) Element</span></span>

<span data-ttu-id="fa86e-105">Contient la valeur associée à un nom dans une paire nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="fa86e-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="fa86e-106">L’élément **value** est défini par le type complexe [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fa86e-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fa86e-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="fa86e-107">Parent element</span></span>



| <span data-ttu-id="fa86e-108">Élément</span><span class="sxs-lookup"><span data-stu-id="fa86e-108">Element</span></span>                                                                                              | <span data-ttu-id="fa86e-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="fa86e-109">Derived from</span></span>                                                       | <span data-ttu-id="fa86e-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa86e-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa86e-111">**ValueQueries (eventTriggerType)**</span><span class="sxs-lookup"><span data-stu-id="fa86e-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="fa86e-112">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="fa86e-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="fa86e-113">Spécifie une collection de requêtes XPath nommées.</span><span class="sxs-lookup"><span data-stu-id="fa86e-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="fa86e-114">Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fa86e-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="fa86e-115">Le nom de la requête peut être utilisé en tant que variable dans le message d’une action ShowMessage.</span><span class="sxs-lookup"><span data-stu-id="fa86e-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fa86e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fa86e-116">Remarks</span></span>

<span data-ttu-id="fa86e-117">Pour le développement C++, consultez la [**propriété Value de ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span><span class="sxs-lookup"><span data-stu-id="fa86e-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="fa86e-118">Pour le développement de scripts, consultez [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).</span><span class="sxs-lookup"><span data-stu-id="fa86e-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa86e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa86e-119">Requirements</span></span>



| <span data-ttu-id="fa86e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa86e-120">Requirement</span></span> | <span data-ttu-id="fa86e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa86e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa86e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa86e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa86e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa86e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa86e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa86e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa86e-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa86e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





