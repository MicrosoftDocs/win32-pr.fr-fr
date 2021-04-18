---
description: La méthode ClearAllGroups supprime tous les groupes de la chronologie, ainsi que tous les objets contenus dans ces groupes.
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'IAMTimeline :: ClearAllGroups, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532826"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="30adc-103">IAMTimeline :: ClearAllGroups, méthode</span><span class="sxs-lookup"><span data-stu-id="30adc-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="30adc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="30adc-104">\[Deprecated.</span></span> <span data-ttu-id="30adc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30adc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30adc-106">La `ClearAllGroups` méthode supprime tous les groupes de la chronologie, ainsi que tous les objets contenus dans ces groupes.</span><span class="sxs-lookup"><span data-stu-id="30adc-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="30adc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30adc-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="30adc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30adc-108">Parameters</span></span>

<span data-ttu-id="30adc-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="30adc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30adc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30adc-110">Return value</span></span>

<span data-ttu-id="30adc-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30adc-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30adc-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30adc-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30adc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="30adc-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30adc-114">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="30adc-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="30adc-115">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="30adc-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="30adc-116">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="30adc-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30adc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30adc-117">Requirements</span></span>



| <span data-ttu-id="30adc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30adc-118">Requirement</span></span> | <span data-ttu-id="30adc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="30adc-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30adc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="30adc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="30adc-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="30adc-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="30adc-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30adc-122">Library</span></span><br/> | <dl> <span data-ttu-id="30adc-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30adc-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30adc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30adc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30adc-125">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="30adc-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="30adc-126">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="30adc-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




