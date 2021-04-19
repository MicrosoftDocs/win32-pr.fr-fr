---
description: La méthode SetMediaTypeForVB spécifie le type de média du groupe pour les clients Automation.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'IAMTimelineGroup :: SetMediaTypeForVB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531063"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="27c30-103">IAMTimelineGroup :: SetMediaTypeForVB, méthode</span><span class="sxs-lookup"><span data-stu-id="27c30-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="27c30-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27c30-104">\[Deprecated.</span></span> <span data-ttu-id="27c30-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27c30-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27c30-106">La `SetMediaTypeForVB` méthode spécifie le type de média du groupe pour les clients Automation.</span><span class="sxs-lookup"><span data-stu-id="27c30-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c30-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27c30-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="27c30-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27c30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c30-109">*Val* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="27c30-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c30-110">Valeur qui spécifie le type de média.</span><span class="sxs-lookup"><span data-stu-id="27c30-110">Value that specifies the media type.</span></span> <span data-ttu-id="27c30-111">Définissez la valeur sur 0 pour Video ou 1 pour audio.</span><span class="sxs-lookup"><span data-stu-id="27c30-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c30-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27c30-112">Return value</span></span>

<span data-ttu-id="27c30-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27c30-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27c30-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27c30-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c30-115">Notes</span><span class="sxs-lookup"><span data-stu-id="27c30-115">Remarks</span></span>

<span data-ttu-id="27c30-116">Cette méthode est destinée aux clients Automation.</span><span class="sxs-lookup"><span data-stu-id="27c30-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="27c30-117">Pour les applications C++, utilisez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="27c30-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="27c30-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="27c30-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27c30-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27c30-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27c30-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27c30-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27c30-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27c30-121">Requirements</span></span>



| <span data-ttu-id="27c30-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27c30-122">Requirement</span></span> | <span data-ttu-id="27c30-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="27c30-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27c30-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="27c30-124">Header</span></span><br/>  | <dl> <span data-ttu-id="27c30-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c30-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27c30-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27c30-126">Library</span></span><br/> | <dl> <span data-ttu-id="27c30-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27c30-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c30-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27c30-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c30-129">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="27c30-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="27c30-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="27c30-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




