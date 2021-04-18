---
description: La \_ méthode obtenir StreamType récupère l’identificateur global unique (Guid) pour le type de média du flux actuel.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'IMediaDet :: get_StreamType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526839"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="72d9a-103">IMediaDet :: \_ StreamType, méthode</span><span class="sxs-lookup"><span data-stu-id="72d9a-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="72d9a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="72d9a-104">\[Deprecated.</span></span> <span data-ttu-id="72d9a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72d9a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72d9a-106">La `get_StreamType` méthode récupère l’identificateur global unique (Guid) pour le type de média du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="72d9a-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d9a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d9a-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="72d9a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d9a-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="72d9a-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="72d9a-110">Reçoit le GUID de type principal pour le type de média.</span><span class="sxs-lookup"><span data-stu-id="72d9a-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d9a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72d9a-111">Return value</span></span>

<span data-ttu-id="72d9a-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72d9a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72d9a-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72d9a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d9a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="72d9a-114">Remarks</span></span>

<span data-ttu-id="72d9a-115">Cette méthode récupère le membre **MajorType** de la structure [**du \_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="72d9a-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="72d9a-116">La structure du **\_ \_ type de média am** décrit le format du flux, et le membre **MajorType** est un GUID qui indique la catégorie générale, telle que l’audio ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="72d9a-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="72d9a-117">Pour un flux vidéo, le GUID est la \_ vidéo de MediaType.</span><span class="sxs-lookup"><span data-stu-id="72d9a-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="72d9a-118">Pour le son, il s’agit de l’audio de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="72d9a-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="72d9a-119">Pour récupérer l’ensemble de la structure du **\_ \_ type de média am** , appelez la méthode [**IMediaDet :: obtenir \_ StreamMediaType**](imediadet-get-streammediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="72d9a-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="72d9a-120">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="72d9a-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="72d9a-121">Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="72d9a-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="72d9a-122">Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="72d9a-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="72d9a-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="72d9a-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72d9a-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72d9a-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72d9a-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="72d9a-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72d9a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d9a-126">Requirements</span></span>



| <span data-ttu-id="72d9a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d9a-127">Requirement</span></span> | <span data-ttu-id="72d9a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d9a-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72d9a-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d9a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="72d9a-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d9a-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72d9a-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72d9a-131">Library</span></span><br/> | <dl> <span data-ttu-id="72d9a-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72d9a-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d9a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d9a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d9a-134">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="72d9a-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="72d9a-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="72d9a-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




