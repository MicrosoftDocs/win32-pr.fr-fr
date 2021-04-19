---
description: 'La méthode GetDefaultFPS récupère la fréquence d’images de sortie par défaut, en images par seconde (FPS). Les groupes utilisent cette valeur comme fréquence d’images par défaut. Pour définir la fréquence d’images d’un groupe, appelez la méthode IAMTimelineGroup :: SetOutputFPS sur le groupe.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'IAMTimeline :: GetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528495"
---
# <a name="iamtimelinegetdefaultfps-method"></a><span data-ttu-id="0287a-105">IAMTimeline :: GetDefaultFPS, méthode</span><span class="sxs-lookup"><span data-stu-id="0287a-105">IAMTimeline::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="0287a-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0287a-106">\[Deprecated.</span></span> <span data-ttu-id="0287a-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0287a-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0287a-108">La `GetDefaultFPS` méthode récupère la fréquence d’images de sortie par défaut, en images par seconde (FPS).</span><span class="sxs-lookup"><span data-stu-id="0287a-108">The `GetDefaultFPS` method retrieves the default output frame rate, in frames per second (FPS).</span></span> <span data-ttu-id="0287a-109">Les groupes utilisent cette valeur comme fréquence d’images par défaut.</span><span class="sxs-lookup"><span data-stu-id="0287a-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="0287a-110">Pour définir la fréquence d’images d’un groupe, appelez la méthode [**IAMTimelineGroup :: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) sur le groupe.</span><span class="sxs-lookup"><span data-stu-id="0287a-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="0287a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0287a-111">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="0287a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0287a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0287a-113">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="0287a-113">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="0287a-114">Reçoit la fréquence d’images par défaut, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="0287a-114">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0287a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0287a-115">Return value</span></span>

<span data-ttu-id="0287a-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0287a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0287a-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0287a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0287a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0287a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0287a-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0287a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0287a-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0287a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0287a-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0287a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0287a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0287a-122">Requirements</span></span>



| <span data-ttu-id="0287a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0287a-123">Requirement</span></span> | <span data-ttu-id="0287a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0287a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0287a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0287a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0287a-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0287a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0287a-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0287a-127">Library</span></span><br/> | <dl> <span data-ttu-id="0287a-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0287a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0287a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0287a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0287a-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="0287a-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="0287a-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0287a-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




