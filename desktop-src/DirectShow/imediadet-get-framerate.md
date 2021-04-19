---
description: La méthode obtenir une fréquence \_ d’images récupère la fréquence d’images du flux actuel. Le flux doit être un flux vidéo.
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'IMediaDet :: get_FrameRate, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525600"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="cf9ba-104">IMediaDet :: obtient la \_ méthode de fréquence</span><span class="sxs-lookup"><span data-stu-id="cf9ba-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="cf9ba-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-105">\[Deprecated.</span></span> <span data-ttu-id="cf9ba-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf9ba-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf9ba-107">La `get_FrameRate` méthode récupère la fréquence d’images du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="cf9ba-108">Le flux doit être un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9ba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf9ba-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cf9ba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf9ba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf9ba-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cf9ba-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf9ba-112">Reçoit la fréquence d’images, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf9ba-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf9ba-113">Return value</span></span>

<span data-ttu-id="cf9ba-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf9ba-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cf9ba-115">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf9ba-115">Possible values include the following:</span></span>



| <span data-ttu-id="cf9ba-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cf9ba-116">Return code</span></span>                                                                                             | <span data-ttu-id="cf9ba-117">Description</span><span class="sxs-lookup"><span data-stu-id="cf9ba-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="cf9ba-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="cf9ba-119">L’en-tête de format vidéo ne spécifie pas de fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="cf9ba-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="cf9ba-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="cf9ba-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="cf9ba-123">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="cf9ba-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="cf9ba-125">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="cf9ba-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="cf9ba-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="cf9ba-127">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="cf9ba-128">Notes</span><span class="sxs-lookup"><span data-stu-id="cf9ba-128">Remarks</span></span>

<span data-ttu-id="cf9ba-129">Cette méthode ne peut pas récupérer la fréquence d’images à partir d’un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="cf9ba-130">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ba-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="cf9ba-131">Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="cf9ba-132">Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ba-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="cf9ba-133">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf9ba-134">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf9ba-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf9ba-135">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cf9ba-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf9ba-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf9ba-136">Requirements</span></span>



| <span data-ttu-id="cf9ba-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf9ba-137">Requirement</span></span> | <span data-ttu-id="cf9ba-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf9ba-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9ba-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf9ba-139">Header</span></span><br/>  | <dl> <span data-ttu-id="cf9ba-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf9ba-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cf9ba-141">Library</span></span><br/> | <dl> <span data-ttu-id="cf9ba-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf9ba-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf9ba-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf9ba-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf9ba-144">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="cf9ba-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="cf9ba-145">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="cf9ba-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




