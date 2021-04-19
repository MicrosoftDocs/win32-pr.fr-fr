---
description: La \_ méthode obtenir StreamMediaType récupère le type de média du flux actuel. Tous les flux vidéo sont convertis en types VIDEOINFOHEADER, et tous les flux audio sont convertis en types WAVEFORMATEX.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'IMediaDet :: get_StreamMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529967"
---
# <a name="imediadetget_streammediatype-method"></a><span data-ttu-id="8e5a0-104">IMediaDet :: \_ StreamMediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="8e5a0-104">IMediaDet::get\_StreamMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="8e5a0-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-105">\[Deprecated.</span></span> <span data-ttu-id="8e5a0-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8e5a0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8e5a0-107">La `get_StreamMediaType` méthode récupère le type de média du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-107">The `get_StreamMediaType` method retrieves the media type of the current stream.</span></span> <span data-ttu-id="8e5a0-108">Tous les flux vidéo sont convertis en types [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , et tous les flux audio sont convertis en types [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8e5a0-108">All video streams are converted to [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) types, and all audio streams are converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) types.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5a0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e5a0-109">Syntax</span></span>


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8e5a0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e5a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e5a0-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8e5a0-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5a0-112">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui est remplie avec le type de média.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e5a0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e5a0-113">Return value</span></span>

<span data-ttu-id="8e5a0-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e5a0-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e5a0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e5a0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8e5a0-116">Remarks</span></span>

<span data-ttu-id="8e5a0-117">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="8e5a0-117">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="8e5a0-118">Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="8e5a0-119">Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="8e5a0-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="8e5a0-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8e5a0-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e5a0-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8e5a0-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8e5a0-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e5a0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e5a0-123">Requirements</span></span>



| <span data-ttu-id="8e5a0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e5a0-124">Requirement</span></span> | <span data-ttu-id="8e5a0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e5a0-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5a0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e5a0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8e5a0-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5a0-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8e5a0-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e5a0-128">Library</span></span><br/> | <dl> <span data-ttu-id="8e5a0-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e5a0-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5a0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e5a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5a0-131">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="8e5a0-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="8e5a0-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="8e5a0-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
