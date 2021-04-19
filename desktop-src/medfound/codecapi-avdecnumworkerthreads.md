---
description: Définit le nombre de threads de travail utilisés par un décodeur vidéo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514966"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="d5c34-103">CODECAPI \_ propriété AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="d5c34-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="d5c34-104">Définit le nombre de threads de travail utilisés par un décodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="d5c34-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="d5c34-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d5c34-105">Data type</span></span>

<span data-ttu-id="d5c34-106">**Long** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="d5c34-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d5c34-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="d5c34-107">Property GUID</span></span>

<span data-ttu-id="d5c34-108">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="d5c34-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c34-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d5c34-109">Remarks</span></span>

<span data-ttu-id="d5c34-110">Si la valeur est 1, le décodeur sélectionne le nombre de threads.</span><span class="sxs-lookup"><span data-stu-id="d5c34-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="d5c34-111">Pour l’interface [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , définissez cette propriété sur une valeur **long** (**VT \_ I4**).</span><span class="sxs-lookup"><span data-stu-id="d5c34-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="d5c34-112">Pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , définissez cette propriété sur **UInt32**, bien que la valeur soit signée.</span><span class="sxs-lookup"><span data-stu-id="d5c34-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c34-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5c34-113">Requirements</span></span>



| <span data-ttu-id="d5c34-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5c34-114">Requirement</span></span> | <span data-ttu-id="d5c34-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5c34-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c34-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5c34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c34-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d5c34-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d5c34-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5c34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c34-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="d5c34-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d5c34-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5c34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c34-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c34-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c34-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5c34-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c34-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5c34-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d5c34-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d5c34-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

