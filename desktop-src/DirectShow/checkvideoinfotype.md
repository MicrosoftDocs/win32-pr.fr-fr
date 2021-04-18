---
description: La fonction CheckVideoInfoType vérifie un type de média qui contient une structure de format VIDEOINFOHEADER pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: CheckVideoInfoType, fonction (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540543"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="ebb09-103">CheckVideoInfoType fonction)</span><span class="sxs-lookup"><span data-stu-id="ebb09-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="ebb09-104">La `CheckVideoInfoType` fonction vérifie un type de média qui contient une structure de format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.</span><span class="sxs-lookup"><span data-stu-id="ebb09-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="ebb09-105">Cette fonction ne garantit pas que le type de média est valide ou que le code qui utilise la structure est sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ebb09-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ebb09-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebb09-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="ebb09-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebb09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb09-108">*crédit*</span><span class="sxs-lookup"><span data-stu-id="ebb09-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ebb09-109">Pointeur vers la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à valider</span><span class="sxs-lookup"><span data-stu-id="ebb09-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebb09-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebb09-110">Return value</span></span>

<span data-ttu-id="ebb09-111">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="ebb09-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="ebb09-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ebb09-112">Return code</span></span>                                                                                                | <span data-ttu-id="ebb09-113">Description</span><span class="sxs-lookup"><span data-stu-id="ebb09-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="ebb09-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebb09-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="ebb09-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ebb09-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="ebb09-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ebb09-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="ebb09-117">Valeur de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="ebb09-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="ebb09-118"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="ebb09-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="ebb09-119">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="ebb09-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ebb09-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ebb09-120">Remarks</span></span>

<span data-ttu-id="ebb09-121">Cette fonction appelle [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) pour valider la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="ebb09-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="ebb09-122">Si le type de format n’est pas le FORMAT \_ videoinfo, la fonction retourne un \_ type VFW E \_ \_ non \_ accepté.</span><span class="sxs-lookup"><span data-stu-id="ebb09-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb09-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebb09-123">Requirements</span></span>



| <span data-ttu-id="ebb09-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebb09-124">Requirement</span></span> | <span data-ttu-id="ebb09-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebb09-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb09-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebb09-126">Header</span></span><br/> | <dl> <span data-ttu-id="ebb09-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebb09-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb09-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebb09-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb09-129">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="ebb09-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




