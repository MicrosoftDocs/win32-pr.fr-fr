---
title: Type complexe InstrumentationType
description: Définit le contenu de la section d’instrumentation du manifeste.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Le type complexe InstrumentationType EventLog
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513033"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="d0e41-104">Type complexe InstrumentationType</span><span class="sxs-lookup"><span data-stu-id="d0e41-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="d0e41-105">Définit le contenu de la section d’instrumentation du manifeste.</span><span class="sxs-lookup"><span data-stu-id="d0e41-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d0e41-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d0e41-106">Child elements</span></span>



| <span data-ttu-id="d0e41-107">Élément</span><span class="sxs-lookup"><span data-stu-id="d0e41-107">Element</span></span>                                                                  | <span data-ttu-id="d0e41-108">Type</span><span class="sxs-lookup"><span data-stu-id="d0e41-108">Type</span></span>                                                             | <span data-ttu-id="d0e41-109">Description</span><span class="sxs-lookup"><span data-stu-id="d0e41-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d0e41-110">**événements**</span><span class="sxs-lookup"><span data-stu-id="d0e41-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="d0e41-111">**EventsType**</span><span class="sxs-lookup"><span data-stu-id="d0e41-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="d0e41-112">Contient une liste de fournisseurs définie par le manifeste.</span><span class="sxs-lookup"><span data-stu-id="d0e41-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d0e41-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0e41-113">Requirements</span></span>



| <span data-ttu-id="d0e41-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0e41-114">Requirement</span></span> | <span data-ttu-id="d0e41-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0e41-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0e41-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e41-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e41-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0e41-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d0e41-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e41-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e41-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0e41-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





