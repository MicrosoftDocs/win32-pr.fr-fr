---
title: ID2D1HwndRenderTarget, méthodes de redimensionnement (D2d1. h)
description: Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Redimensionner les méthodes Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537107"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="957e3-104">ID2D1HwndRenderTarget :: Resize, méthodes</span><span class="sxs-lookup"><span data-stu-id="957e3-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="957e3-105">Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="957e3-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="957e3-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="957e3-106">Overload list</span></span>



| <span data-ttu-id="957e3-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="957e3-107">Method</span></span>                                                                         | <span data-ttu-id="957e3-108">Description</span><span class="sxs-lookup"><span data-stu-id="957e3-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="957e3-109">[**Redimensionner ( \_ taille d2d1 \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="957e3-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="957e3-110">Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="957e3-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="957e3-111">[**Redimensionner (D2D1 \_ taille \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="957e3-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="957e3-112">Modifie la taille de la cible de rendu avec la taille de pixel spécifiée.</span><span class="sxs-lookup"><span data-stu-id="957e3-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="957e3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="957e3-113">Remarks</span></span>

<span data-ttu-id="957e3-114">Après l’appel de cette méthode, le contenu de la mémoire tampon d’arrière-plan de la cible de rendu n’est pas défini, même si l’option [**d2d1 présente l’option \_ conserver le \_ \_ \_ contenu**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) a été spécifiée lors de la création de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="957e3-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="957e3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="957e3-115">Requirements</span></span>



| <span data-ttu-id="957e3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="957e3-116">Requirement</span></span> | <span data-ttu-id="957e3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="957e3-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="957e3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="957e3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="957e3-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="957e3-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="957e3-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="957e3-120">Library</span></span><br/> | <dl> <span data-ttu-id="957e3-121"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="957e3-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="957e3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="957e3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="957e3-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="957e3-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957e3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="957e3-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="957e3-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="957e3-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="957e3-126">�</span><span class="sxs-lookup"><span data-stu-id="957e3-126">�</span></span>

<span data-ttu-id="957e3-127">�</span><span class="sxs-lookup"><span data-stu-id="957e3-127">�</span></span>
