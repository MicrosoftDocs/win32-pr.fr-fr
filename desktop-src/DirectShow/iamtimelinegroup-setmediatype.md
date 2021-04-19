---
description: La méthode SetMediaType définit le type de média non compressé pour le groupe.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'IAMTimelineGroup :: SetMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525603"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="bdbda-103">IAMTimelineGroup :: SetMediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="bdbda-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="bdbda-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bdbda-104">\[Deprecated.</span></span> <span data-ttu-id="bdbda-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bdbda-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bdbda-106">La `SetMediaType` méthode définit le type de média non compressé pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="bdbda-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdbda-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="bdbda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdbda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbda-109">*PMT* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bdbda-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbda-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) décrivant le format.</span><span class="sxs-lookup"><span data-stu-id="bdbda-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbda-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bdbda-111">Return value</span></span>

<span data-ttu-id="bdbda-112">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="bdbda-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="bdbda-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bdbda-113">Return code</span></span>                                                                                             | <span data-ttu-id="bdbda-114">Description</span><span class="sxs-lookup"><span data-stu-id="bdbda-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="bdbda-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbda-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="bdbda-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="bdbda-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="bdbda-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbda-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="bdbda-118">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="bdbda-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="bdbda-119"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbda-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="bdbda-120">Le type de média spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bdbda-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdbda-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bdbda-121">Remarks</span></span>

<span data-ttu-id="bdbda-122">Les types de média suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="bdbda-122">The following media types are supported:</span></span>

-   <span data-ttu-id="bdbda-123">Vidéo RVB non compressée</span><span class="sxs-lookup"><span data-stu-id="bdbda-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="bdbda-124">16 bits par pixel, format 555 (MEDIASUBTYPE \_ RGB555)</span><span class="sxs-lookup"><span data-stu-id="bdbda-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="bdbda-125">24 bits par pixel (MEDIASUBTYPE \_ Rgb24)</span><span class="sxs-lookup"><span data-stu-id="bdbda-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="bdbda-126">32 bits par pixel, avec alpha (MEDIASUBTYPE \_ ARGB32, et non MEDIASUBTYPE \_ RGB32)</span><span class="sxs-lookup"><span data-stu-id="bdbda-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="bdbda-127">audio PCM stéréo 16 bits (MEDIASUBTYPE \_ PCM)</span><span class="sxs-lookup"><span data-stu-id="bdbda-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="bdbda-128">Les types de vidéos doivent utiliser \_ le format videoinfo pour le type de format et [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="bdbda-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="bdbda-129">Le format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bdbda-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="bdbda-130">En outre, les formats vidéo descendants (*biheight* < 0) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bdbda-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="bdbda-131">Pour spécifier un format de compression pour le groupe, appelez la méthode [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="bdbda-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="bdbda-132">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bdbda-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bdbda-133">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bdbda-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bdbda-134">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bdbda-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bdbda-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdbda-135">Requirements</span></span>



| <span data-ttu-id="bdbda-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bdbda-136">Requirement</span></span> | <span data-ttu-id="bdbda-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="bdbda-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbda-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="bdbda-138">Header</span></span><br/>  | <dl> <span data-ttu-id="bdbda-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbda-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bdbda-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bdbda-140">Library</span></span><br/> | <dl> <span data-ttu-id="bdbda-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdbda-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdbda-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdbda-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbda-143">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="bdbda-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="bdbda-144">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="bdbda-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




