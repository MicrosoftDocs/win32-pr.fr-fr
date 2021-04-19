---
description: La méthode GetImageSize récupère les informations sur la taille de l’image vidéo.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Méthode CBaseControlVideo. GetImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545700"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="7696d-103">Méthode CBaseControlVideo. GetImageSize</span><span class="sxs-lookup"><span data-stu-id="7696d-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="7696d-104">La `GetImageSize` méthode récupère les informations sur la taille de l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="7696d-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7696d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7696d-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="7696d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7696d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7696d-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="7696d-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7696d-108">Pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à remplir.</span><span class="sxs-lookup"><span data-stu-id="7696d-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="7696d-109">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="7696d-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7696d-110">Pointeur vers la taille de la mémoire tampon vidéo.</span><span class="sxs-lookup"><span data-stu-id="7696d-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7696d-111">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="7696d-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="7696d-112">Pointeur vers les dimensions du rectangle de la vidéo source.</span><span class="sxs-lookup"><span data-stu-id="7696d-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7696d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7696d-113">Return value</span></span>

<span data-ttu-id="7696d-114">Retourne une valeur **HRESULT** qui dépend de l’implémentation de. Il peut s’agir de l’une des valeurs suivantes ou d’autres valeurs non listées.</span><span class="sxs-lookup"><span data-stu-id="7696d-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="7696d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7696d-115">Return code</span></span>                                                                                  | <span data-ttu-id="7696d-116">Description</span><span class="sxs-lookup"><span data-stu-id="7696d-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7696d-117"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="7696d-118">Échec.</span><span class="sxs-lookup"><span data-stu-id="7696d-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7696d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7696d-120">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="7696d-120">Invalid argument.</span></span> <span data-ttu-id="7696d-121">Le format de données n’est pas compatible.</span><span class="sxs-lookup"><span data-stu-id="7696d-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="7696d-122"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="7696d-123">Une erreur inattendue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="7696d-123">Unexpected error occurred.</span></span> <span data-ttu-id="7696d-124">Un ou plusieurs arguments ont la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7696d-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="7696d-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="7696d-126">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7696d-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7696d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="7696d-127">Remarks</span></span>

<span data-ttu-id="7696d-128">Cette fonction membre est une fonction d’assistance utilisée pour créer des rendus d’image mémoire d’images DIB.</span><span class="sxs-lookup"><span data-stu-id="7696d-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="7696d-129">Elle est appelée à partir de l’implémentation de la classe de base de [**CBaseControlVideo :: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) lorsqu’un paramètre _pVideoImage_ **null** est passé à cette fonction membre.</span><span class="sxs-lookup"><span data-stu-id="7696d-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="7696d-130">Par conséquent, cette fonction membre construit et retourne une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , à l’aide des informations contenues dans *pBufferSize* et *pSourceRect*.</span><span class="sxs-lookup"><span data-stu-id="7696d-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="7696d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7696d-131">Requirements</span></span>



| <span data-ttu-id="7696d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7696d-132">Requirement</span></span> | <span data-ttu-id="7696d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7696d-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7696d-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7696d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7696d-135"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7696d-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7696d-136">Library</span></span><br/> | <dl> <span data-ttu-id="7696d-137"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7696d-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7696d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7696d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7696d-139">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="7696d-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




