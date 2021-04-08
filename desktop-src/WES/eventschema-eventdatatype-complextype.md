---
title: Type complexe EventDataType
description: Définit les éléments de données d’événement et les structures qui contiennent les données d’événement.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType type complexe EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740373"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="9effc-104">Type complexe EventDataType</span><span class="sxs-lookup"><span data-stu-id="9effc-104">EventDataType Complex Type</span></span>

<span data-ttu-id="9effc-105">Définit les éléments de données d’événement et les structures qui contiennent les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="9effc-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9effc-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9effc-106">Child elements</span></span>



| <span data-ttu-id="9effc-107">Élément</span><span class="sxs-lookup"><span data-stu-id="9effc-107">Element</span></span>                                                              | <span data-ttu-id="9effc-108">Type</span><span class="sxs-lookup"><span data-stu-id="9effc-108">Type</span></span>                                                               | <span data-ttu-id="9effc-109">Description</span><span class="sxs-lookup"><span data-stu-id="9effc-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9effc-110">**Binary**</span><span class="sxs-lookup"><span data-stu-id="9effc-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="9effc-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="9effc-111">hexBinary</span></span>                                                          | <span data-ttu-id="9effc-112">Objet blob de données binaires pour les événements écrits à l’aide de la [journalisation des événements](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="9effc-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="9effc-113">**ComplexData**</span><span class="sxs-lookup"><span data-stu-id="9effc-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="9effc-114">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="9effc-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="9effc-115">Structure définie dans le modèle pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="9effc-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="9effc-116">**Données**</span><span class="sxs-lookup"><span data-stu-id="9effc-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="9effc-117">**DataType**</span><span class="sxs-lookup"><span data-stu-id="9effc-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="9effc-118">Élément de données de niveau supérieur défini dans le modèle pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="9effc-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="9effc-119">Attributs</span><span class="sxs-lookup"><span data-stu-id="9effc-119">Attributes</span></span>



| <span data-ttu-id="9effc-120">Nom</span><span class="sxs-lookup"><span data-stu-id="9effc-120">Name</span></span> | <span data-ttu-id="9effc-121">Type</span><span class="sxs-lookup"><span data-stu-id="9effc-121">Type</span></span>   | <span data-ttu-id="9effc-122">Description</span><span class="sxs-lookup"><span data-stu-id="9effc-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="9effc-123">Nom</span><span class="sxs-lookup"><span data-stu-id="9effc-123">Name</span></span> | <span data-ttu-id="9effc-124">string</span><span class="sxs-lookup"><span data-stu-id="9effc-124">string</span></span> | <span data-ttu-id="9effc-125">Nom du modèle qui contient les éléments de données.</span><span class="sxs-lookup"><span data-stu-id="9effc-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9effc-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9effc-126">Remarks</span></span>

<span data-ttu-id="9effc-127">La fonction [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) affiche des tableaux et des structures sous forme d’objets BLOB binaires.</span><span class="sxs-lookup"><span data-stu-id="9effc-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9effc-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9effc-128">Requirements</span></span>



| <span data-ttu-id="9effc-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9effc-129">Requirement</span></span> | <span data-ttu-id="9effc-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9effc-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9effc-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9effc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9effc-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9effc-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9effc-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9effc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9effc-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9effc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

