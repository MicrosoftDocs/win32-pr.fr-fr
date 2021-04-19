---
description: La méthode SetOutputFPS définit la fréquence d’images de sortie non compressées pour ce groupe.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'IAMTimelineGroup :: SetOutputFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545608"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="c871a-103">IAMTimelineGroup :: SetOutputFPS, méthode</span><span class="sxs-lookup"><span data-stu-id="c871a-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="c871a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c871a-104">\[Deprecated.</span></span> <span data-ttu-id="c871a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c871a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c871a-106">La `SetOutputFPS` méthode définit la fréquence d’images de sortie non compressées pour ce groupe.</span><span class="sxs-lookup"><span data-stu-id="c871a-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="c871a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c871a-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="c871a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c871a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c871a-109">*i/s*</span><span class="sxs-lookup"><span data-stu-id="c871a-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="c871a-110">Fréquence d’images de sortie pour ce groupe, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="c871a-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="c871a-111">La valeur ne peut pas être égale à zéro et ne peut pas comporter plus de sept chiffres après la virgule.</span><span class="sxs-lookup"><span data-stu-id="c871a-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c871a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c871a-112">Return value</span></span>

<span data-ttu-id="c871a-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c871a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c871a-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c871a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c871a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c871a-115">Remarks</span></span>

<span data-ttu-id="c871a-116">Le rendu de la sortie de ce groupe s’exécute à la fréquence d’images spécifiée, et toutes les modifications sur le matériel source sont arrondies à la limite d’image la plus proche, comme défini par la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="c871a-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="c871a-117">Pour des performances optimales, utilisez la même fréquence d’images pour tous les groupes, vidéo et audio.</span><span class="sxs-lookup"><span data-stu-id="c871a-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="c871a-118">La méthode [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) remplace la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="c871a-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="c871a-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c871a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c871a-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c871a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c871a-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c871a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c871a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c871a-122">Requirements</span></span>



| <span data-ttu-id="c871a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c871a-123">Requirement</span></span> | <span data-ttu-id="c871a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c871a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c871a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c871a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c871a-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c871a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c871a-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c871a-127">Library</span></span><br/> | <dl> <span data-ttu-id="c871a-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c871a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c871a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c871a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c871a-130">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="c871a-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="c871a-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="c871a-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




