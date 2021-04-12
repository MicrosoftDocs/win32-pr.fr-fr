---
title: D2D1_TAG (D2d1. h)
description: Valeur 64 bits définie par l’application et utilisée pour \ 160 ; marquez un ensemble d’opérations de rendu.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317206"
---
# <a name="d2d1_tag"></a><span data-ttu-id="157de-104">\_Balise d2d1</span><span class="sxs-lookup"><span data-stu-id="157de-104">D2D1\_TAG</span></span>

<span data-ttu-id="157de-105">Valeur 64 bits définie par l’application, utilisée pour marquer un ensemble d’opérations de rendu.</span><span class="sxs-lookup"><span data-stu-id="157de-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="157de-106">Notes</span><span class="sxs-lookup"><span data-stu-id="157de-106">Remarks</span></span>

<span data-ttu-id="157de-107">Pour définir une balise avant une série d’opérations de rendu, utilisez la méthode [**ID2D1RenderTarget :: SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="157de-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="157de-108">Pour récupérer la balise active, utilisez la méthode [**ID2D1RenderTarget :: GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .</span><span class="sxs-lookup"><span data-stu-id="157de-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="157de-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="157de-109">Requirements</span></span>



| <span data-ttu-id="157de-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="157de-110">Requirement</span></span> | <span data-ttu-id="157de-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="157de-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="157de-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="157de-112">Minimum supported client</span></span><br/> | <span data-ttu-id="157de-113">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="157de-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="157de-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="157de-114">Minimum supported server</span></span><br/> | <span data-ttu-id="157de-115">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="157de-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="157de-116">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="157de-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="157de-117">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="157de-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="157de-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="157de-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="157de-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="157de-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="157de-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="157de-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="157de-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="157de-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="157de-122">**SetTags**</span><span class="sxs-lookup"><span data-stu-id="157de-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

