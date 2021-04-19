---
description: La \_ méthode obtenir StreamLength récupère la durée du flux actuel.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'IMediaDet :: get_StreamLength, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531056"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="3fbc1-103">IMediaDet :: \_ StreamLength, méthode</span><span class="sxs-lookup"><span data-stu-id="3fbc1-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="3fbc1-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-104">\[Deprecated.</span></span> <span data-ttu-id="3fbc1-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3fbc1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3fbc1-106">La `get_StreamLength` méthode récupère la durée du flux actuel.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbc1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fbc1-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3fbc1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fbc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbc1-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3fbc1-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3fbc1-110">Reçoit la durée du flux, en secondes.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbc1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fbc1-111">Return value</span></span>

<span data-ttu-id="3fbc1-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3fbc1-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3fbc1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fbc1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3fbc1-114">Remarks</span></span>

<span data-ttu-id="3fbc1-115">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="3fbc1-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="3fbc1-116">Si le détecteur de média est en mode de manipulation bitmap, cette méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="3fbc1-117">Pour plus d’informations, consultez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="3fbc1-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="3fbc1-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3fbc1-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3fbc1-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3fbc1-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3fbc1-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fbc1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fbc1-121">Requirements</span></span>



| <span data-ttu-id="3fbc1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fbc1-122">Requirement</span></span> | <span data-ttu-id="3fbc1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fbc1-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbc1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fbc1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3fbc1-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fbc1-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3fbc1-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3fbc1-126">Library</span></span><br/> | <dl> <span data-ttu-id="3fbc1-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fbc1-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fbc1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fbc1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbc1-129">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="3fbc1-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="3fbc1-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3fbc1-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




