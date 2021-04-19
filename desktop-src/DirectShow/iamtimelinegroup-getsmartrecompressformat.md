---
description: La méthode GetSmartRecompressFormat récupère le format de compression actuel pour la recompression intelligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'IAMTimelineGroup :: GetSmartRecompressFormat, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530968"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="20a8c-103">IAMTimelineGroup :: GetSmartRecompressFormat, méthode</span><span class="sxs-lookup"><span data-stu-id="20a8c-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="20a8c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="20a8c-104">\[Deprecated.</span></span> <span data-ttu-id="20a8c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="20a8c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="20a8c-106">La `GetSmartRecompressFormat` méthode récupère le format de compression actuel pour la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="20a8c-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a8c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20a8c-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="20a8c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20a8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a8c-109">*ppFormat*</span><span class="sxs-lookup"><span data-stu-id="20a8c-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="20a8c-110">Reçoit un pointeur vers une structure [**SCompFmt0**](scompfmt0.md) , casté en un pointeur vers une valeur long.</span><span class="sxs-lookup"><span data-stu-id="20a8c-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="20a8c-111">Si la méthode échoue, la valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="20a8c-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a8c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20a8c-112">Return value</span></span>

<span data-ttu-id="20a8c-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="20a8c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20a8c-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20a8c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a8c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="20a8c-115">Remarks</span></span>

<span data-ttu-id="20a8c-116">Si l’application n’a pas défini de format de compression intelligente (en appelant [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), le format retourné par cette méthode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="20a8c-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="20a8c-117">Appelez la méthode [**IAMTimelineGroup :: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) pour déterminer si un format de compression a été défini.</span><span class="sxs-lookup"><span data-stu-id="20a8c-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="20a8c-118">Si la méthode est réussie, l’appelant doit libérer le type de média retourné et supprimer la structure [**SCompFmt0**](scompfmt0.md) :</span><span class="sxs-lookup"><span data-stu-id="20a8c-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="20a8c-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="20a8c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="20a8c-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="20a8c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="20a8c-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="20a8c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20a8c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a8c-122">Requirements</span></span>



| <span data-ttu-id="20a8c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a8c-123">Requirement</span></span> | <span data-ttu-id="20a8c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a8c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20a8c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="20a8c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="20a8c-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="20a8c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="20a8c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20a8c-127">Library</span></span><br/> | <dl> <span data-ttu-id="20a8c-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20a8c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20a8c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a8c-130">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="20a8c-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="20a8c-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="20a8c-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




