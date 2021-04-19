---
description: La méthode SetStreamNumber spécifie le flux à lire à partir du fichier source associé à cet objet source.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'IAMTimelineSrc :: SetStreamNumber, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541399"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="8bf87-103">IAMTimelineSrc :: SetStreamNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="8bf87-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="8bf87-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="8bf87-104">\[Deprecated.</span></span> <span data-ttu-id="8bf87-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8bf87-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8bf87-106">La `SetStreamNumber` méthode spécifie le flux à lire à partir du fichier source associé à cet objet source.</span><span class="sxs-lookup"><span data-stu-id="8bf87-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bf87-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="8bf87-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8bf87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf87-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="8bf87-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf87-110">Numéro de flux, à partir de l’ensemble de flux correspondant au type de média du groupe parent.</span><span class="sxs-lookup"><span data-stu-id="8bf87-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf87-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8bf87-111">Return value</span></span>

<span data-ttu-id="8bf87-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8bf87-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bf87-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8bf87-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf87-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8bf87-114">Remarks</span></span>

<span data-ttu-id="8bf87-115">Le paramètre *Val* spécifie un numéro de flux à partir de l’ensemble de flux qui correspond au type de média du groupe parent, et non à partir de l’ensemble des flux dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="8bf87-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="8bf87-116">Par exemple, supposons qu’un fichier contienne deux flux vidéo et deux flux audio.</span><span class="sxs-lookup"><span data-stu-id="8bf87-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="8bf87-117">Si l’objet source est à l’intérieur d’un groupe vidéo, l’affectation de la valeur 0 à *Val* sélectionne le premier flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="8bf87-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="8bf87-118">L’appelant est chargé de spécifier un numéro de flux valide.</span><span class="sxs-lookup"><span data-stu-id="8bf87-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="8bf87-119">Le nombre de flux est défini par défaut sur zéro.</span><span class="sxs-lookup"><span data-stu-id="8bf87-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="8bf87-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="8bf87-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8bf87-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8bf87-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8bf87-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8bf87-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8bf87-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8bf87-123">Requirements</span></span>



| <span data-ttu-id="8bf87-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8bf87-124">Requirement</span></span> | <span data-ttu-id="8bf87-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bf87-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf87-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8bf87-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8bf87-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf87-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8bf87-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8bf87-128">Library</span></span><br/> | <dl> <span data-ttu-id="8bf87-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bf87-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf87-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bf87-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf87-131">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="8bf87-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="8bf87-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="8bf87-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




