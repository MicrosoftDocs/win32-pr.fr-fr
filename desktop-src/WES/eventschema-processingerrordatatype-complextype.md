---
title: Type complexe ProcessingErrorDataType
description: Définit une erreur qui s’est produite lors du rendu des données d’événement pour l’événement.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- ProcessingErrorDataType type complexe EventLog
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105178"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="22711-104">Type complexe ProcessingErrorDataType</span><span class="sxs-lookup"><span data-stu-id="22711-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="22711-105">Définit une erreur qui s’est produite lors du rendu des données d’événement pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="22711-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="22711-106">Cela peut se produire si les données d’événement ne correspondent pas à la définition du modèle de données d’événement dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="22711-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
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

## <a name="child-elements"></a><span data-ttu-id="22711-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="22711-107">Child elements</span></span>



| <span data-ttu-id="22711-108">Élément</span><span class="sxs-lookup"><span data-stu-id="22711-108">Element</span></span>                                                                          | <span data-ttu-id="22711-109">Type</span><span class="sxs-lookup"><span data-stu-id="22711-109">Type</span></span>        | <span data-ttu-id="22711-110">Description</span><span class="sxs-lookup"><span data-stu-id="22711-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="22711-111">**Nom de l'élément de données**</span><span class="sxs-lookup"><span data-stu-id="22711-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="22711-112">string</span><span class="sxs-lookup"><span data-stu-id="22711-112">string</span></span>      | <span data-ttu-id="22711-113">Nom de l’élément de données d’événement à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="22711-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="22711-114">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22711-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="22711-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="22711-115">unsignedInt</span></span> | <span data-ttu-id="22711-116">Code d’erreur de l’erreur qui s’est produite lors du rendu des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="22711-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="22711-117">**EventPayload**</span><span class="sxs-lookup"><span data-stu-id="22711-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="22711-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="22711-118">hexBinary</span></span>   | <span data-ttu-id="22711-119">Objet blob binaire qui contient l’intégralité des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="22711-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="22711-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22711-120">Requirements</span></span>



| <span data-ttu-id="22711-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22711-121">Requirement</span></span> | <span data-ttu-id="22711-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="22711-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22711-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22711-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22711-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22711-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22711-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22711-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22711-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22711-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





