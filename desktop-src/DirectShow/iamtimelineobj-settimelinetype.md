---
description: 'Non pris en charge. Appelez la méthode IAMTimeline :: CreateEmptyNode pour créer un nouvel objet Timeline. Une fois qu’un objet est créé, vous ne pouvez pas modifier son type.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'IAMTimelineObj :: SetTimelineType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541656"
---
# <a name="iamtimelineobjsettimelinetype-method"></a><span data-ttu-id="f002a-105">IAMTimelineObj :: SetTimelineType, méthode</span><span class="sxs-lookup"><span data-stu-id="f002a-105">IAMTimelineObj::SetTimelineType method</span></span>

> [!Note]  
> <span data-ttu-id="f002a-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f002a-106">\[Deprecated.</span></span> <span data-ttu-id="f002a-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f002a-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f002a-108">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f002a-108">Not supported.</span></span> <span data-ttu-id="f002a-109">Appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) pour créer un nouvel objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="f002a-109">Call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method to create a new timeline object.</span></span> <span data-ttu-id="f002a-110">Une fois qu’un objet est créé, vous ne pouvez pas modifier son type.</span><span class="sxs-lookup"><span data-stu-id="f002a-110">Once an object is created, you cannot change its type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f002a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f002a-111">Syntax</span></span>


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f002a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f002a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f002a-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="f002a-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f002a-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f002a-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f002a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f002a-115">Return value</span></span>

<span data-ttu-id="f002a-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f002a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f002a-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f002a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f002a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f002a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f002a-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f002a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f002a-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f002a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f002a-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f002a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f002a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f002a-122">Requirements</span></span>



| <span data-ttu-id="f002a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f002a-123">Requirement</span></span> | <span data-ttu-id="f002a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f002a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f002a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f002a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f002a-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f002a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f002a-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f002a-127">Library</span></span><br/> | <dl> <span data-ttu-id="f002a-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f002a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f002a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f002a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f002a-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f002a-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> </dl>

 

 




