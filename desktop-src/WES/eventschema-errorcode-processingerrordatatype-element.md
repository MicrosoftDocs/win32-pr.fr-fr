---
title: ErrorCode (élément ProcessingErrorDataType)
description: Contient le code d’erreur qui a été déclenché lorsqu’une erreur s’est produite lors du traitement des données d’événement.
ms.assetid: 30243369-6ab0-450b-a345-6f8ff9b21543
keywords:
- ErrorCode, élément EventLog
topic_type:
- apiref
api_name:
- ErrorCode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 938870f5069c2be920bf6b9a7970d76f89620e68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384015"
---
# <a name="errorcode-processingerrordatatype-element"></a><span data-ttu-id="b8167-104">ErrorCode (élément ProcessingErrorDataType)</span><span class="sxs-lookup"><span data-stu-id="b8167-104">ErrorCode (ProcessingErrorDataType) Element</span></span>

<span data-ttu-id="b8167-105">Contient le code d’erreur qui a été déclenché lorsqu’une erreur s’est produite lors du traitement des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="b8167-105">Contains the error code that was raised when there was an error processing event data.</span></span>

``` syntax
<xs:element name="ErrorCode"
    type="unsignedInt"
 />
```

<span data-ttu-id="b8167-106">L’élément **ErrorCode** est défini par le type complexe [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b8167-106">The **ErrorCode** element is defined by the [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8167-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8167-107">Requirements</span></span>



| <span data-ttu-id="b8167-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8167-108">Requirement</span></span> | <span data-ttu-id="b8167-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8167-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8167-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8167-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b8167-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8167-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8167-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8167-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b8167-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8167-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8167-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8167-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8167-115">**Élément parent**</span><span class="sxs-lookup"><span data-stu-id="b8167-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="b8167-116">**ProcessingErrorData (EventType)**</span><span class="sxs-lookup"><span data-stu-id="b8167-116">**ProcessingErrorData (EventType)**</span></span>](eventschema-processingerrordata-eventtype-element.md)
</dt> </dl>

 

 





