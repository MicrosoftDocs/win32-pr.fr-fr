---
description: La \_ méthode obtenir OutputStreams récupère le nombre de flux audio et vidéo contenus dans la source du média. Tous les autres types de flux, tels que les flux de données, sont ignorés.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'IMediaDet :: get_OutputStreams, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526817"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="0a1f9-104">IMediaDet :: \_ OutputStreams, méthode</span><span class="sxs-lookup"><span data-stu-id="0a1f9-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="0a1f9-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-105">\[Deprecated.</span></span> <span data-ttu-id="0a1f9-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a1f9-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a1f9-107">La `get_OutputStreams` méthode récupère le nombre de flux audio et vidéo contenus dans la source du média.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="0a1f9-108">Tous les autres types de flux, tels que les flux de données, sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1f9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a1f9-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0a1f9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a1f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a1f9-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0a1f9-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1f9-112">Reçoit le nombre de flux de sortie.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a1f9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a1f9-113">Return value</span></span>

<span data-ttu-id="0a1f9-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a1f9-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a1f9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a1f9-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0a1f9-116">Remarks</span></span>

<span data-ttu-id="0a1f9-117">Avant d’appeler cette méthode, appelez [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) pour définir le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="0a1f9-118">Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="0a1f9-119">Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="0a1f9-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a1f9-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a1f9-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0a1f9-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a1f9-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0a1f9-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a1f9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a1f9-123">Requirements</span></span>



| <span data-ttu-id="0a1f9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a1f9-124">Requirement</span></span> | <span data-ttu-id="0a1f9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a1f9-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1f9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a1f9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0a1f9-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a1f9-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a1f9-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a1f9-128">Library</span></span><br/> | <dl> <span data-ttu-id="0a1f9-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a1f9-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a1f9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a1f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1f9-131">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="0a1f9-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="0a1f9-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0a1f9-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




