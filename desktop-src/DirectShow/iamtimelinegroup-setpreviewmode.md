---
description: La méthode SetPreviewMode définit le mode Aperçu pour le groupe.
ms.assetid: 40b7e9ac-30b3-454e-82ac-10ac99f1b86f
title: 'IAMTimelineGroup :: SetPreviewMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetPreviewMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fe03e6be3572b6cc660e51c27551a316db990d80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541452"
---
# <a name="iamtimelinegroupsetpreviewmode-method"></a><span data-ttu-id="8e931-103">IAMTimelineGroup :: SetPreviewMode, méthode</span><span class="sxs-lookup"><span data-stu-id="8e931-103">IAMTimelineGroup::SetPreviewMode method</span></span>

> [!Note]  
> <span data-ttu-id="8e931-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8e931-104">\[Deprecated.</span></span> <span data-ttu-id="8e931-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8e931-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8e931-106">La méthode SetPreviewMode définit le mode Aperçu pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="8e931-106">The SetPreviewMode method sets the preview mode for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e931-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e931-107">Syntax</span></span>


```C++
HRESULT SetPreviewMode(
   BOOL fPreview
);
```



## <a name="parameters"></a><span data-ttu-id="8e931-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e931-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e931-109">*fPreview*</span><span class="sxs-lookup"><span data-stu-id="8e931-109">*fPreview*</span></span> 
</dt> <dd>

<span data-ttu-id="8e931-110">Mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="8e931-110">The preview mode.</span></span> <span data-ttu-id="8e931-111">Si la **valeur est true**, le groupe est en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="8e931-111">If **TRUE**, the group is in preview mode.</span></span> <span data-ttu-id="8e931-112">Si la **valeur est false**, le groupe est en mode création.</span><span class="sxs-lookup"><span data-stu-id="8e931-112">If **FALSE**, the group is in authoring mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e931-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e931-113">Return value</span></span>

<span data-ttu-id="8e931-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e931-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e931-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e931-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e931-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8e931-116">Remarks</span></span>

<span data-ttu-id="8e931-117">En mode aperçu, les images sont supprimées pendant les effets lents ou les transitions pour maintenir la vidéo synchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="8e931-117">In preview mode, frames are dropped during slow effects or transitions to keep the video synchronized with the audio.</span></span> <span data-ttu-id="8e931-118">La vidéo peut paraître hachée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="8e931-118">The video might look choppy as a result.</span></span> <span data-ttu-id="8e931-119">En mode création, chaque frame est rendu.</span><span class="sxs-lookup"><span data-stu-id="8e931-119">In authoring mode, every frame is rendered.</span></span> <span data-ttu-id="8e931-120">Le mode création est approprié pour l’écriture de fichiers ; pour l’aperçu à l’écran, la vidéo peut ne pas être synchronisée avec l’audio.</span><span class="sxs-lookup"><span data-stu-id="8e931-120">Authoring mode is appropriate for writing files; for on-screen preview, the video might be out of sync with the audio.</span></span>

> [!Note]  
> <span data-ttu-id="8e931-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8e931-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8e931-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8e931-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8e931-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8e931-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e931-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e931-124">Requirements</span></span>



| <span data-ttu-id="8e931-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e931-125">Requirement</span></span> | <span data-ttu-id="8e931-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e931-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e931-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e931-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8e931-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e931-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8e931-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e931-129">Library</span></span><br/> | <dl> <span data-ttu-id="8e931-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e931-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e931-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e931-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e931-132">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="8e931-132">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="8e931-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="8e931-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




