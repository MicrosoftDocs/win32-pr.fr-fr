---
title: EventID (élément SystemPropertiesType)
description: Identificateur que le fournisseur a utilisé pour identifier l’événement.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- EventID, élément EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464562"
---
# <a name="eventid-systempropertiestype-element"></a><span data-ttu-id="62043-104">EventID (élément SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="62043-104">EventID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="62043-105">Identificateur que le fournisseur a utilisé pour identifier l’événement.</span><span class="sxs-lookup"><span data-stu-id="62043-105">The identifier that the provider used to identify the event.</span></span>

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="62043-106">L’élément **eventID** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="62043-106">The **EventID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="62043-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62043-107">Requirements</span></span>



| <span data-ttu-id="62043-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62043-108">Requirement</span></span> | <span data-ttu-id="62043-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="62043-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62043-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62043-110">Minimum supported client</span></span><br/> | <span data-ttu-id="62043-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62043-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="62043-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62043-112">Minimum supported server</span></span><br/> | <span data-ttu-id="62043-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62043-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62043-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62043-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="62043-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="62043-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="62043-116">**Système (EventType)**</span><span class="sxs-lookup"><span data-stu-id="62043-116">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





