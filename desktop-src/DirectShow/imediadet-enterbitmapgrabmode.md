---
description: La méthode EnterBitmapGrabMode bascule le détecteur de média en mode de manipulation bitmap et recherche le graphique de filtre à une heure spécifiée.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'IMediaDet :: EnterBitmapGrabMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542367"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="657a3-103">IMediaDet :: EnterBitmapGrabMode, méthode</span><span class="sxs-lookup"><span data-stu-id="657a3-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="657a3-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="657a3-104">\[Deprecated.</span></span> <span data-ttu-id="657a3-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="657a3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="657a3-106">La `EnterBitmapGrabMode` méthode bascule le détecteur de média en mode de manipulation bitmap et recherche le graphique de filtre à une heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="657a3-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="657a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="657a3-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="657a3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="657a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657a3-109">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="657a3-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="657a3-110">Durée, en secondes, à laquelle le graphique recherche.</span><span class="sxs-lookup"><span data-stu-id="657a3-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657a3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="657a3-111">Return value</span></span>

<span data-ttu-id="657a3-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="657a3-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="657a3-113">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="657a3-113">Possible values include the following:</span></span>



| <span data-ttu-id="657a3-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="657a3-114">Return code</span></span>                                                                                             | <span data-ttu-id="657a3-115">Description</span><span class="sxs-lookup"><span data-stu-id="657a3-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="657a3-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="657a3-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="657a3-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="657a3-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="657a3-119">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="657a3-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="657a3-120"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="657a3-121">Le fichier source n’a pas de flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="657a3-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="657a3-122"><dt>**VFW \_ E \_ temps \_ expiré**</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="657a3-123">Délai d’attente de la commande Seek dépassé.</span><span class="sxs-lookup"><span data-stu-id="657a3-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="657a3-124">Notes</span><span class="sxs-lookup"><span data-stu-id="657a3-124">Remarks</span></span>

<span data-ttu-id="657a3-125">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="657a3-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="657a3-126">Cette méthode insère l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="657a3-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="657a3-127">Vous pouvez ensuite appeler [**IMediaDet :: GetSampleGrabber**](imediadet-getsamplegrabber.md) pour obtenir un pointeur vers l’interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="657a3-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="657a3-128">Une fois que le détecteur de média passe en mode de manipulation bitmap, les différentes méthodes d’information dans **IMediaDet** ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="657a3-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="657a3-129">Les méthodes [**IMediaDet :: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet :: WriteBitmapBits**](imediadet-writebitmapbits.md) placent également le détecteur de média en mode de manipulation bitmap.</span><span class="sxs-lookup"><span data-stu-id="657a3-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="657a3-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="657a3-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="657a3-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="657a3-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="657a3-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="657a3-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="657a3-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="657a3-133">Requirements</span></span>



| <span data-ttu-id="657a3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="657a3-134">Requirement</span></span> | <span data-ttu-id="657a3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="657a3-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="657a3-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="657a3-136">Header</span></span><br/>  | <dl> <span data-ttu-id="657a3-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="657a3-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="657a3-138">Library</span></span><br/> | <dl> <span data-ttu-id="657a3-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="657a3-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657a3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="657a3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657a3-141">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="657a3-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="657a3-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="657a3-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




