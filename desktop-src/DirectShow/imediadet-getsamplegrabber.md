---
description: La méthode GetSampleGrabber récupère un pointeur vers l’interface ISampleGrabber, qui permet à une application de récupérer des échantillons individuels à partir d’un flux de média.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'IMediaDet :: GetSampleGrabber, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526077"
---
# <a name="imediadetgetsamplegrabber-method"></a><span data-ttu-id="5f2ef-103">IMediaDet :: GetSampleGrabber, méthode</span><span class="sxs-lookup"><span data-stu-id="5f2ef-103">IMediaDet::GetSampleGrabber method</span></span>

> [!Note]  
> <span data-ttu-id="5f2ef-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-104">\[Deprecated.</span></span> <span data-ttu-id="5f2ef-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f2ef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5f2ef-106">La `GetSampleGrabber` méthode récupère un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) , qui permet à une application de récupérer des échantillons individuels à partir d’un flux de média.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-106">The `GetSampleGrabber` method retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface, which enables an application to retrieve individual samples from a media stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2ef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f2ef-107">Syntax</span></span>


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="5f2ef-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f2ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f2ef-109">*ppVal* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f2ef-109">*ppVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2ef-110">Reçoit un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="5f2ef-110">Receives a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f2ef-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f2ef-111">Return value</span></span>

<span data-ttu-id="5f2ef-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f2ef-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f2ef-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f2ef-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5f2ef-114">Remarks</span></span>

<span data-ttu-id="5f2ef-115">Appelez [**IMediaDet :: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-115">Call [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) before calling this method.</span></span> <span data-ttu-id="5f2ef-116">L’interface [**ISampleGrabber**](isamplegrabber.md) vous permet de récupérer des échantillons de médias individuels à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-116">The [**ISampleGrabber**](isamplegrabber.md) interface enables you to retrieve individual media samples from the stream.</span></span> <span data-ttu-id="5f2ef-117">Si vous avez simplement besoin d’une image bitmap d’une image vidéo, appelez la méthode [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-117">If you just need a bitmap from a video frame, call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method instead.</span></span> <span data-ttu-id="5f2ef-118">L’interface **ISampleGrabber** est plus souple, mais elle nécessite plus de travail que l’application.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-118">The **ISampleGrabber** interface is more flexible, but requires more work by the application.</span></span>

<span data-ttu-id="5f2ef-119">Si cette méthode est réussie, l’interface [**ISampleGrabber**](isamplegrabber.md) qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-119">If this method succeeds, the [**ISampleGrabber**](isamplegrabber.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="5f2ef-120">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="5f2ef-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5f2ef-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5f2ef-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5f2ef-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5f2ef-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f2ef-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f2ef-124">Requirements</span></span>



| <span data-ttu-id="5f2ef-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f2ef-125">Requirement</span></span> | <span data-ttu-id="5f2ef-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f2ef-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2ef-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f2ef-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5f2ef-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ef-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5f2ef-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f2ef-129">Library</span></span><br/> | <dl> <span data-ttu-id="5f2ef-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ef-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2ef-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f2ef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2ef-132">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="5f2ef-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="5f2ef-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="5f2ef-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




