---
description: La \_ méthode put MediaType définit le type de média de sortie sur le filtre de redimensionnement.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: IResize ::p ut_MediaType, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526060"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="07479-103">IResize ::p ut \_ MediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="07479-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="07479-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="07479-104">\[Deprecated.</span></span> <span data-ttu-id="07479-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07479-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="07479-106">La `put_MediaType` méthode définit le type de média de sortie sur le filtre de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="07479-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="07479-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07479-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="07479-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07479-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07479-109">*PMT* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="07479-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07479-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui contient le type de média.</span><span class="sxs-lookup"><span data-stu-id="07479-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07479-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07479-111">Return value</span></span>

<span data-ttu-id="07479-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="07479-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07479-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07479-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="07479-114">Notes</span><span class="sxs-lookup"><span data-stu-id="07479-114">Remarks</span></span>

<span data-ttu-id="07479-115">DES appelle cette méthode avant de connecter la broche de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="07479-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="07479-116">Utilisez le type de média comme type de média de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="07479-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="07479-117">Retournez ce type de média dans la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) et vérifiez agsint ce type dans la méthode [**CTransformFilter :: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="07479-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="07479-118">DES n’appelle jamais cette méthode une fois que la broche de sortie est connectée.</span><span class="sxs-lookup"><span data-stu-id="07479-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="07479-119">Actuellement, le définit toujours le type de média de sortie sur un format RVB non compressé avec un bloc de format **VIDEOINFOHEADER** (le type de format est égal au format \_ videoinfo).</span><span class="sxs-lookup"><span data-stu-id="07479-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="07479-120">Le sous-type peut être MEDIASUBTYPE \_ ARGB32, qui indique la couleur rvb 32 bits avec un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="07479-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="07479-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="07479-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="07479-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="07479-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="07479-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="07479-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07479-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07479-124">Requirements</span></span>



| <span data-ttu-id="07479-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07479-125">Requirement</span></span> | <span data-ttu-id="07479-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="07479-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07479-127">Version</span><span class="sxs-lookup"><span data-stu-id="07479-127">Version</span></span><br/> | <span data-ttu-id="07479-128">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="07479-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="07479-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="07479-129">Header</span></span><br/>  | <dl> <span data-ttu-id="07479-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="07479-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="07479-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="07479-131">Library</span></span><br/> | <dl> <span data-ttu-id="07479-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07479-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07479-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07479-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07479-134">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="07479-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="07479-135">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="07479-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




