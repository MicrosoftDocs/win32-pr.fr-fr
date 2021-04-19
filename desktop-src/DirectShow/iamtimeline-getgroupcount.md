---
description: La méthode GetGroupCount récupère le nombre de groupes contenus dans la chronologie.
ms.assetid: 24351e03-3132-4363-8171-eae517fb770a
title: 'IAMTimeline :: GetGroupCount, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroupCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4d16cf44839b05f39bc747cb89eda77842caa04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543866"
---
# <a name="iamtimelinegetgroupcount-method"></a><span data-ttu-id="734d4-103">IAMTimeline :: GetGroupCount, méthode</span><span class="sxs-lookup"><span data-stu-id="734d4-103">IAMTimeline::GetGroupCount method</span></span>

> [!Note]  
> <span data-ttu-id="734d4-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="734d4-104">\[Deprecated.</span></span> <span data-ttu-id="734d4-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="734d4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="734d4-106">La `GetGroupCount` méthode récupère le nombre de groupes contenus dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="734d4-106">The `GetGroupCount` method retrieves the number of groups that are contained in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="734d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="734d4-107">Syntax</span></span>


```C++
HRESULT GetGroupCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="734d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="734d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="734d4-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="734d4-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="734d4-110">Reçoit le nombre de groupes dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="734d4-110">Receives the number of groups in the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="734d4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="734d4-111">Return value</span></span>

<span data-ttu-id="734d4-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="734d4-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="734d4-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="734d4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="734d4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="734d4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="734d4-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="734d4-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="734d4-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="734d4-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="734d4-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="734d4-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="734d4-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="734d4-118">Requirements</span></span>



| <span data-ttu-id="734d4-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="734d4-119">Requirement</span></span> | <span data-ttu-id="734d4-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="734d4-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="734d4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="734d4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="734d4-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="734d4-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="734d4-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="734d4-123">Library</span></span><br/> | <dl> <span data-ttu-id="734d4-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="734d4-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="734d4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="734d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="734d4-126">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="734d4-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="734d4-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="734d4-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




