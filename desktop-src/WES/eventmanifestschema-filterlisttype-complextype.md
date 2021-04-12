---
title: Type complexe FilterListType
description: Définit une liste de filtres qu’un contrôleur ETW peut passer à votre fournisseur pour limiter davantage les événements qu’il écrit.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- FilterListType type complexe EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317462"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="59a1a-104">Type complexe FilterListType</span><span class="sxs-lookup"><span data-stu-id="59a1a-104">FilterListType Complex Type</span></span>

<span data-ttu-id="59a1a-105">Définit une liste de filtres qu’un contrôleur ETW peut passer à votre fournisseur pour limiter davantage les événements qu’il écrit.</span><span class="sxs-lookup"><span data-stu-id="59a1a-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="59a1a-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="59a1a-106">Child elements</span></span>



| <span data-ttu-id="59a1a-107">Élément</span><span class="sxs-lookup"><span data-stu-id="59a1a-107">Element</span></span>    | <span data-ttu-id="59a1a-108">Type</span><span class="sxs-lookup"><span data-stu-id="59a1a-108">Type</span></span>                                                             | <span data-ttu-id="59a1a-109">Description</span><span class="sxs-lookup"><span data-stu-id="59a1a-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="59a1a-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="59a1a-110">**filter**</span></span> | [<span data-ttu-id="59a1a-111">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="59a1a-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="59a1a-112">Liste de filtres.</span><span class="sxs-lookup"><span data-stu-id="59a1a-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="59a1a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="59a1a-113">Remarks</span></span>

<span data-ttu-id="59a1a-114">Un contrôleur ETW est une application qui appelle la fonction [**StartTrace**](/windows/desktop/ETW/starttrace) pour créer une session ETW.</span><span class="sxs-lookup"><span data-stu-id="59a1a-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="59a1a-115">Pour plus d’informations, consultez [contrôle des sessions de suivi d’événements](/windows/desktop/ETW/controlling-event-tracing-sessions).</span><span class="sxs-lookup"><span data-stu-id="59a1a-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="59a1a-116">Le contrôleur peut utiliser la fonction [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) pour énumérer les filtres que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="59a1a-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="59a1a-117">Le contrôleur peut alors passer un ou plusieurs filtres lorsqu’il appelle la fonction [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) pour activer votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="59a1a-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="59a1a-118">Votre fournisseur reçoit les filtres, ainsi que le reste des paramètres Enable, dans votre fonction de rappel [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .</span><span class="sxs-lookup"><span data-stu-id="59a1a-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a1a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59a1a-119">Requirements</span></span>



| <span data-ttu-id="59a1a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59a1a-120">Requirement</span></span> | <span data-ttu-id="59a1a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="59a1a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="59a1a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59a1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59a1a-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59a1a-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="59a1a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59a1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59a1a-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59a1a-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

