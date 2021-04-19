---
description: La fonction CheckVideoInfo2Type vérifie un type de média qui contient une structure de format VIDEOINFOHEADER2 pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: CheckVideoInfo2Type, fonction (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537548"
---
# <a name="checkvideoinfo2type-function"></a><span data-ttu-id="c4261-103">CheckVideoInfo2Type fonction)</span><span class="sxs-lookup"><span data-stu-id="c4261-103">CheckVideoInfo2Type function</span></span>

<span data-ttu-id="c4261-104">La `CheckVideoInfo2Type` fonction vérifie un type de média qui contient une structure de format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.</span><span class="sxs-lookup"><span data-stu-id="c4261-104">The `CheckVideoInfo2Type` function checks a media type that contains a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="c4261-105">Cette fonction ne garantit pas que le type de média est valide ou que le code qui utilise la structure est sécurisé.</span><span class="sxs-lookup"><span data-stu-id="c4261-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c4261-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4261-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="c4261-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4261-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4261-108">*crédit*</span><span class="sxs-lookup"><span data-stu-id="c4261-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c4261-109">Pointeur vers la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à valider.</span><span class="sxs-lookup"><span data-stu-id="c4261-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4261-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4261-110">Return value</span></span>

<span data-ttu-id="c4261-111">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="c4261-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="c4261-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c4261-112">Return code</span></span>                                                                                                | <span data-ttu-id="c4261-113">Description</span><span class="sxs-lookup"><span data-stu-id="c4261-113">Description</span></span>                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="c4261-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4261-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c4261-115">Succès</span><span class="sxs-lookup"><span data-stu-id="c4261-115">Success</span></span><br/>                |
| <dl> <span data-ttu-id="c4261-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c4261-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="c4261-117">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="c4261-117">**NULL** pointer value</span></span><br/> |
| <dl> <span data-ttu-id="c4261-118"><dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt></span><span class="sxs-lookup"><span data-stu-id="c4261-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="c4261-119">Type de média non valide</span><span class="sxs-lookup"><span data-stu-id="c4261-119">Invalid media type</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c4261-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c4261-120">Remarks</span></span>

<span data-ttu-id="c4261-121">Cette fonction appelle [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) pour valider la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le type de média.</span><span class="sxs-lookup"><span data-stu-id="c4261-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="c4261-122">Si le type de format n’est pas le **format \_ VideoInfo2**, la fonction retourne un **\_ type VFW E \_ \_ non \_ accepté**.</span><span class="sxs-lookup"><span data-stu-id="c4261-122">If the format type is not **FORMAT\_VideoInfo2**, the function returns **VFW\_E\_TYPE\_NOT\_ACCEPTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4261-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4261-123">Requirements</span></span>



| <span data-ttu-id="c4261-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4261-124">Requirement</span></span> | <span data-ttu-id="c4261-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4261-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4261-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4261-126">Header</span></span><br/> | <dl> <span data-ttu-id="c4261-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4261-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4261-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4261-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4261-129">Fonctions vidéo et image</span><span class="sxs-lookup"><span data-stu-id="c4261-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




