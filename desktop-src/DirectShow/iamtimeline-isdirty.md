---
description: Non pris en charge.
ms.assetid: ed6fd633-23b8-4b80-901c-d7b50fa4c15e
title: 'IAMTimeline :: IsDirty, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.IsDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d5281a4caa0a559e64ac9d7ccb2ff46b5285c491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525429"
---
# <a name="iamtimelineisdirty-method"></a><span data-ttu-id="6a4ac-103">IAMTimeline :: IsDirty, méthode</span><span class="sxs-lookup"><span data-stu-id="6a4ac-103">IAMTimeline::IsDirty method</span></span>

> [!Note]  
> <span data-ttu-id="6a4ac-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-104">\[Deprecated.</span></span> <span data-ttu-id="6a4ac-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a4ac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6a4ac-106">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a4ac-107">Syntax</span></span>


```C++
HRESULT IsDirty(
   BOOL *pDirty
);
```



## <a name="parameters"></a><span data-ttu-id="6a4ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a4ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4ac-109">*pDirty*</span><span class="sxs-lookup"><span data-stu-id="6a4ac-109">*pDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="6a4ac-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a4ac-111">Return value</span></span>

<span data-ttu-id="6a4ac-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a4ac-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a4ac-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4ac-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6a4ac-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a4ac-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6a4ac-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6a4ac-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6a4ac-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6a4ac-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a4ac-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a4ac-118">Requirements</span></span>



| <span data-ttu-id="6a4ac-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a4ac-119">Requirement</span></span> | <span data-ttu-id="6a4ac-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a4ac-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4ac-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a4ac-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6a4ac-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6a4ac-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a4ac-123">Library</span></span><br/> | <dl> <span data-ttu-id="6a4ac-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a4ac-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4ac-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a4ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4ac-126">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="6a4ac-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




