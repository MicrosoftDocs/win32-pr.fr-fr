---
description: La méthode SetStretchMode définit le mode Stretch. Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'IAMTimelineSrc :: SetStretchMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532751"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="9ee87-104">IAMTimelineSrc :: SetStretchMode, méthode</span><span class="sxs-lookup"><span data-stu-id="9ee87-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="9ee87-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9ee87-105">\[Deprecated.</span></span> <span data-ttu-id="9ee87-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ee87-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ee87-107">La `SetStretchMode` méthode définit le mode Stretch.</span><span class="sxs-lookup"><span data-stu-id="9ee87-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="9ee87-108">Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.</span><span class="sxs-lookup"><span data-stu-id="9ee87-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ee87-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ee87-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="9ee87-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ee87-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ee87-111">*nStretchMode*</span><span class="sxs-lookup"><span data-stu-id="9ee87-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="9ee87-112">Indicateur qui spécifie le mode d’étirement actuel.</span><span class="sxs-lookup"><span data-stu-id="9ee87-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="9ee87-113">Pour obtenir la liste des valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9ee87-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ee87-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ee87-114">Return value</span></span>

<span data-ttu-id="9ee87-115">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ee87-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ee87-116">Notes</span><span class="sxs-lookup"><span data-stu-id="9ee87-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ee87-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9ee87-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ee87-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ee87-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ee87-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ee87-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ee87-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ee87-120">Requirements</span></span>



| <span data-ttu-id="9ee87-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ee87-121">Requirement</span></span> | <span data-ttu-id="9ee87-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ee87-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ee87-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ee87-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9ee87-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ee87-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ee87-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ee87-125">Library</span></span><br/> | <dl> <span data-ttu-id="9ee87-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ee87-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ee87-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ee87-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ee87-128">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="9ee87-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="9ee87-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="9ee87-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




