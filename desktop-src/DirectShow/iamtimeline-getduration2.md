---
description: 'La méthode GetDuration2 récupère la durée de la chronologie. Cette méthode est équivalente à IAMTimeline :: GetDuration, mais prend un paramètre de type double.'
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: 'IAMTimeline :: GetDuration2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528764"
---
# <a name="iamtimelinegetduration2-method"></a><span data-ttu-id="fa08c-104">IAMTimeline :: GetDuration2, méthode</span><span class="sxs-lookup"><span data-stu-id="fa08c-104">IAMTimeline::GetDuration2 method</span></span>

> [!Note]  
> <span data-ttu-id="fa08c-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fa08c-105">\[Deprecated.</span></span> <span data-ttu-id="fa08c-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa08c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa08c-107">La `GetDuration2` méthode récupère la durée de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="fa08c-107">The `GetDuration2` method retrieves the duration of the timeline.</span></span> <span data-ttu-id="fa08c-108">Cette méthode est équivalente à [**IAMTimeline :: GetDuration**](iamtimeline-getduration.md), mais prend un paramètre de type **double**.</span><span class="sxs-lookup"><span data-stu-id="fa08c-108">This method is equivalent to [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), but takes a parameter of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa08c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa08c-109">Syntax</span></span>


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="fa08c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa08c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa08c-111">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="fa08c-111">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="fa08c-112">Reçoit la durée de la chronologie, en fractions de seconde.</span><span class="sxs-lookup"><span data-stu-id="fa08c-112">Receives the duration of the timeline, in fractional seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa08c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa08c-113">Return value</span></span>

<span data-ttu-id="fa08c-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa08c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa08c-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa08c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa08c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fa08c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa08c-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="fa08c-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa08c-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa08c-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa08c-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fa08c-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa08c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa08c-120">Requirements</span></span>



| <span data-ttu-id="fa08c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa08c-121">Requirement</span></span> | <span data-ttu-id="fa08c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa08c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa08c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa08c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fa08c-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa08c-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa08c-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa08c-125">Library</span></span><br/> | <dl> <span data-ttu-id="fa08c-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa08c-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa08c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa08c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa08c-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="fa08c-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="fa08c-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="fa08c-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




