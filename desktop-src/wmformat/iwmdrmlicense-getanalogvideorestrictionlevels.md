---
title: Méthode IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: La méthode GetAnalogVideoRestrictionLevels récupère toutes les restrictions de la vidéo analogique définies sur la licence actuelle.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Méthode GetAnalogVideoRestrictionLevels format Windows Media
- Méthode GetAnalogVideoRestrictionLevels format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539683"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="f2697-106">IWMDRMLicense :: GetAnalogVideoRestrictionLevels, méthode</span><span class="sxs-lookup"><span data-stu-id="f2697-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="f2697-107">La méthode **GetAnalogVideoRestrictionLevels** récupère toutes les restrictions de la vidéo analogique définies sur la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="f2697-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2697-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2697-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="f2697-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2697-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2697-110">*\[ rgAnalogVideoRestrictions \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="f2697-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2697-111">Reçoit un tableau de structures de [**\_ \_ \_ restrictions de vidéo analogiques WMDRM**](wmdrm-analog-video-restrictions.md) .</span><span class="sxs-lookup"><span data-stu-id="f2697-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="f2697-112">Affectez la valeur **null** pour récupérer le nombre d’éléments du tableau dans *pcResctrictions*.</span><span class="sxs-lookup"><span data-stu-id="f2697-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="f2697-113">*pcRestrictions* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f2697-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2697-114">Nombre d’éléments dans le tableau de restrictions.</span><span class="sxs-lookup"><span data-stu-id="f2697-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="f2697-115">Si *rgAnalogVideoRestrictions* a la valeur **null**, cette valeur est définie sur le nombre d’éléments nécessaires dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f2697-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2697-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2697-116">Return value</span></span>

<span data-ttu-id="f2697-117">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f2697-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f2697-118">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2697-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f2697-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f2697-119">Return code</span></span>                                                                          | <span data-ttu-id="f2697-120">Description</span><span class="sxs-lookup"><span data-stu-id="f2697-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f2697-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f2697-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f2697-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2697-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2697-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f2697-123">Remarks</span></span>

<span data-ttu-id="f2697-124">Vous devez allouer de la mémoire pour le tableau de restrictions.</span><span class="sxs-lookup"><span data-stu-id="f2697-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="f2697-125">Pour ce faire, appelez d’abord la méthode avec *rgAnalogVideoRestrictions* défini sur **null**, ce qui affectera à *pcRestrictions* la valeur du nombre d’éléments requis.</span><span class="sxs-lookup"><span data-stu-id="f2697-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2697-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2697-126">Requirements</span></span>



| <span data-ttu-id="f2697-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2697-127">Requirement</span></span> | <span data-ttu-id="f2697-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2697-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2697-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2697-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f2697-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2697-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2697-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2697-131">Library</span></span><br/> | <dl> <span data-ttu-id="f2697-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2697-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2697-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2697-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2697-134">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="f2697-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





