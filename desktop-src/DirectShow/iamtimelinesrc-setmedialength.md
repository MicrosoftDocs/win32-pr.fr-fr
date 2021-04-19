---
description: La méthode SetMediaLength spécifie la durée du fichier source.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'IAMTimelineSrc :: SetMediaLength, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543933"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="41063-103">IAMTimelineSrc :: SetMediaLength, méthode</span><span class="sxs-lookup"><span data-stu-id="41063-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="41063-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="41063-104">\[Deprecated.</span></span> <span data-ttu-id="41063-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41063-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41063-106">La `SetMediaLength` méthode spécifie la durée du fichier source.</span><span class="sxs-lookup"><span data-stu-id="41063-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="41063-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41063-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="41063-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41063-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41063-109">*Durée*</span><span class="sxs-lookup"><span data-stu-id="41063-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="41063-110">Longueur du média, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="41063-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41063-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41063-111">Return value</span></span>

<span data-ttu-id="41063-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41063-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41063-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41063-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41063-114">Notes</span><span class="sxs-lookup"><span data-stu-id="41063-114">Remarks</span></span>

<span data-ttu-id="41063-115">Vous pouvez éviter les erreurs de rendu potentielles en définissant la longueur du support avant de définir l’heure d’arrêt du support.</span><span class="sxs-lookup"><span data-stu-id="41063-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="41063-116">Lorsque vous définissez l’heure d’arrêt du support, l’algorithme DES le vérifie par rapport à la longueur du support.</span><span class="sxs-lookup"><span data-stu-id="41063-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="41063-117">Cette méthode ne valide pas le paramètre de *longueur* , mais la valeur doit être égale à la durée réelle du fichier source.</span><span class="sxs-lookup"><span data-stu-id="41063-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="41063-118">Obtenez la durée du fichier source en appelant [**IMediaDet :: obtenir \_ StreamLength**](imediadet-get-streamlength.md).</span><span class="sxs-lookup"><span data-stu-id="41063-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="41063-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="41063-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="41063-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="41063-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="41063-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="41063-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41063-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41063-122">Requirements</span></span>



| <span data-ttu-id="41063-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41063-123">Requirement</span></span> | <span data-ttu-id="41063-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="41063-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41063-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="41063-125">Header</span></span><br/>  | <dl> <span data-ttu-id="41063-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="41063-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="41063-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41063-127">Library</span></span><br/> | <dl> <span data-ttu-id="41063-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41063-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41063-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41063-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41063-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="41063-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="41063-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="41063-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




