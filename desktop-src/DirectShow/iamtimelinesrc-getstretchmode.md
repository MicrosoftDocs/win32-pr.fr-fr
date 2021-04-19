---
description: La méthode GetStretchMode récupère le mode Stretch. Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'IAMTimelineSrc :: GetStretchMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521744"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a><span data-ttu-id="3c941-104">IAMTimelineSrc :: GetStretchMode, méthode</span><span class="sxs-lookup"><span data-stu-id="3c941-104">IAMTimelineSrc::GetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="3c941-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3c941-105">\[Deprecated.</span></span> <span data-ttu-id="3c941-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c941-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c941-107">La `GetStretchMode` méthode récupère le mode Stretch.</span><span class="sxs-lookup"><span data-stu-id="3c941-107">The `GetStretchMode` method retrieves the stretch mode.</span></span> <span data-ttu-id="3c941-108">Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.</span><span class="sxs-lookup"><span data-stu-id="3c941-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c941-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c941-109">Syntax</span></span>


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="3c941-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c941-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c941-111">*pnStretchMode*</span><span class="sxs-lookup"><span data-stu-id="3c941-111">*pnStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3c941-112">Reçoit un indicateur qui spécifie le mode d’étirement actuel.</span><span class="sxs-lookup"><span data-stu-id="3c941-112">Receives a flag indicating the current stretch mode.</span></span> <span data-ttu-id="3c941-113">Pour obtenir la liste des valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3c941-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c941-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c941-114">Return value</span></span>

<span data-ttu-id="3c941-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c941-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c941-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c941-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c941-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3c941-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c941-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3c941-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c941-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3c941-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3c941-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3c941-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c941-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c941-121">Requirements</span></span>



| <span data-ttu-id="3c941-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c941-122">Requirement</span></span> | <span data-ttu-id="3c941-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c941-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c941-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c941-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3c941-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c941-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3c941-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c941-126">Library</span></span><br/> | <dl> <span data-ttu-id="3c941-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c941-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c941-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c941-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c941-129">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="3c941-129">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="3c941-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3c941-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




