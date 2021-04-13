---
description: Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propriété AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482513"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="af611-103">Propriété AVEncCommonPassEnd</span><span class="sxs-lookup"><span data-stu-id="af611-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="af611-104">Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.</span><span class="sxs-lookup"><span data-stu-id="af611-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="af611-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="af611-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="af611-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="af611-106">Data type</span></span>

<span data-ttu-id="af611-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="af611-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="af611-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="af611-108">Property GUID</span></span>

<span data-ttu-id="af611-109">**CODECAPI \_ AVEncCommonPassEnd**</span><span class="sxs-lookup"><span data-stu-id="af611-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="af611-110">Notes</span><span class="sxs-lookup"><span data-stu-id="af611-110">Remarks</span></span>

<span data-ttu-id="af611-111">L’affectation de la **\_ valeur variant** à cette propriété met fin à la passe d’encodage en cours.</span><span class="sxs-lookup"><span data-stu-id="af611-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="af611-112">L’affectation de la **\_ valeur false** à cette propriété met fin à l’encodage multipasse.</span><span class="sxs-lookup"><span data-stu-id="af611-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="af611-113">La lecture de cette propriété demande si le passage de l’encodage actuel est le dernier.</span><span class="sxs-lookup"><span data-stu-id="af611-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="af611-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af611-114">Requirements</span></span>



| <span data-ttu-id="af611-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af611-115">Requirement</span></span> | <span data-ttu-id="af611-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="af611-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af611-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af611-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af611-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="af611-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="af611-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af611-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af611-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="af611-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="af611-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="af611-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af611-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af611-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af611-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af611-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af611-124">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="af611-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="af611-125">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="af611-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




