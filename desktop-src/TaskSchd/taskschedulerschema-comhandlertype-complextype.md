---
title: Type complexe comHandlerType
description: Définit les éléments enfants et les informations de séquencement pour l’élément comgérer.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- Planificateur de tâches de type complexe comHandlerType
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032648"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="4ccd3-104">Type complexe comHandlerType</span><span class="sxs-lookup"><span data-stu-id="4ccd3-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="4ccd3-105">Définit les éléments enfants et les informations de séquencement pour l’élément [**comgérer**](taskschedulerschema-comhandler-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4ccd3-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4ccd3-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4ccd3-106">Child elements</span></span>



| <span data-ttu-id="4ccd3-107">Élément</span><span class="sxs-lookup"><span data-stu-id="4ccd3-107">Element</span></span>                                                               | <span data-ttu-id="4ccd3-108">Type</span><span class="sxs-lookup"><span data-stu-id="4ccd3-108">Type</span></span>                                                         | <span data-ttu-id="4ccd3-109">Description</span><span class="sxs-lookup"><span data-stu-id="4ccd3-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="4ccd3-110">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="4ccd3-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="4ccd3-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="4ccd3-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="4ccd3-112">Spécifie l’identificateur de la classe de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="4ccd3-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="4ccd3-113">**Données**</span><span class="sxs-lookup"><span data-stu-id="4ccd3-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="4ccd3-114">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="4ccd3-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="4ccd3-115">Spécifie des données supplémentaires associées au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="4ccd3-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="4ccd3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ccd3-116">Requirements</span></span>



| <span data-ttu-id="4ccd3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ccd3-117">Requirement</span></span> | <span data-ttu-id="4ccd3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ccd3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ccd3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ccd3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccd3-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ccd3-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4ccd3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ccd3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccd3-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ccd3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ccd3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ccd3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccd3-124">Types complexes de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4ccd3-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="4ccd3-125">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="4ccd3-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





