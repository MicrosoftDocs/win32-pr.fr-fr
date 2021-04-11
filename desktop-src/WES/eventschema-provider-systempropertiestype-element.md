---
title: Élément Provider (SystemPropertiesType)
description: Identifie le fournisseur qui a consigné l’événement.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- EventLog, élément EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032513"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="71eaa-104">Élément Provider (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="71eaa-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="71eaa-105">Identifie le fournisseur qui a consigné l’événement.</span><span class="sxs-lookup"><span data-stu-id="71eaa-105">Identifies the provider that logged the event.</span></span>

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="71eaa-106">L’élément **Provider** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="71eaa-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="71eaa-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="71eaa-107">Attributes</span></span>



| <span data-ttu-id="71eaa-108">Nom</span><span class="sxs-lookup"><span data-stu-id="71eaa-108">Name</span></span>            | <span data-ttu-id="71eaa-109">Type</span><span class="sxs-lookup"><span data-stu-id="71eaa-109">Type</span></span>                                                | <span data-ttu-id="71eaa-110">Description</span><span class="sxs-lookup"><span data-stu-id="71eaa-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71eaa-111">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="71eaa-111">EventSourceName</span></span> | <span data-ttu-id="71eaa-112">string</span><span class="sxs-lookup"><span data-stu-id="71eaa-112">string</span></span>                                              | <span data-ttu-id="71eaa-113">Nom de la source d’événements qui a publié l’événement (si la source de l’événement provient de l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) héritée).</span><span class="sxs-lookup"><span data-stu-id="71eaa-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="71eaa-114">Guid</span><span class="sxs-lookup"><span data-stu-id="71eaa-114">Guid</span></span>            | [<span data-ttu-id="71eaa-115">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="71eaa-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="71eaa-116">Identificateur global unique qui identifie le fournisseur de manière unique.</span><span class="sxs-lookup"><span data-stu-id="71eaa-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="71eaa-117">Nom</span><span class="sxs-lookup"><span data-stu-id="71eaa-117">Name</span></span>            | <span data-ttu-id="71eaa-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="71eaa-118">anyURI</span></span>                                              | <span data-ttu-id="71eaa-119">Nom du fournisseur d’événements qui a consigné l’événement.</span><span class="sxs-lookup"><span data-stu-id="71eaa-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="71eaa-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71eaa-120">Requirements</span></span>



| <span data-ttu-id="71eaa-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71eaa-121">Requirement</span></span> | <span data-ttu-id="71eaa-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="71eaa-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="71eaa-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71eaa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="71eaa-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71eaa-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="71eaa-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71eaa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="71eaa-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71eaa-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71eaa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71eaa-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="71eaa-128">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="71eaa-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="71eaa-129">**Système (EventType)**</span><span class="sxs-lookup"><span data-stu-id="71eaa-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

