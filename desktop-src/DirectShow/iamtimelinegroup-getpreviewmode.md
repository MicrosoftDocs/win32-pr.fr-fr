---
description: La méthode GetPreviewMode récupère le mode Aperçu pour le groupe.
ms.assetid: 635354e5-5cb2-4045-8a7f-21d31005c5f3
title: 'IAMTimelineGroup :: GetPreviewMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 724c35c57ff90216547a8a343b469cb627e32415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544498"
---
# <a name="iamtimelinegroupgetpreviewmode-method"></a><span data-ttu-id="b6a17-103">IAMTimelineGroup :: GetPreviewMode, méthode</span><span class="sxs-lookup"><span data-stu-id="b6a17-103">IAMTimelineGroup::GetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="b6a17-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b6a17-104">\[Deprecated.</span></span> <span data-ttu-id="b6a17-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6a17-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b6a17-106">La `GetPreviewMode` méthode récupère le mode Aperçu pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="b6a17-106">The `GetPreviewMode` method retrieves the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6a17-107">Syntax</span></span>


```C++
HRESULT GetPreviewMode(
   BOOL *pfPreview
);
```



## <a name="parameters"></a><span data-ttu-id="b6a17-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6a17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6a17-109">*pfPreview*</span><span class="sxs-lookup"><span data-stu-id="b6a17-109">*pfPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="b6a17-110">Reçoit une valeur booléenne indiquant le mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="b6a17-110">Receives a Boolean value indicating the preview mode.</span></span> <span data-ttu-id="b6a17-111">Si la **valeur est true**, le groupe est en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="b6a17-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="b6a17-112">Si la **valeur est false**, le groupe est en mode création.</span><span class="sxs-lookup"><span data-stu-id="b6a17-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6a17-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6a17-113">Return value</span></span>

<span data-ttu-id="b6a17-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b6a17-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6a17-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6a17-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a17-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b6a17-116">Remarks</span></span>

<span data-ttu-id="b6a17-117">En mode aperçu, les images sont supprimées pendant les effets lents ou les transitions pour maintenir la vidéo synchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="b6a17-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="b6a17-118">La vidéo peut paraître hachée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="b6a17-118">The video might look choppy as a result.</span></span> <span data-ttu-id="b6a17-119">En mode création, chaque frame est rendu.</span><span class="sxs-lookup"><span data-stu-id="b6a17-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="b6a17-120">Le mode création est approprié pour l’écriture de fichiers ; pour l’aperçu à l’écran, la vidéo peut être désynchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="b6a17-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might become out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="b6a17-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b6a17-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b6a17-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6a17-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b6a17-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b6a17-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6a17-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6a17-124">Requirements</span></span>



| <span data-ttu-id="b6a17-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6a17-125">Requirement</span></span> | <span data-ttu-id="b6a17-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6a17-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a17-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6a17-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b6a17-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6a17-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b6a17-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6a17-129">Library</span></span><br/> | <dl> <span data-ttu-id="b6a17-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6a17-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a17-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6a17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a17-132">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="b6a17-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="b6a17-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b6a17-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




