---
description: La méthode GetMediaType récupère le type de média non compressé pour le groupe.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'IAMTimelineGroup :: GetMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526486"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="22d3a-103">IAMTimelineGroup :: GetMediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="22d3a-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="22d3a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="22d3a-104">\[Deprecated.</span></span> <span data-ttu-id="22d3a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="22d3a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22d3a-106">La `GetMediaType` méthode récupère le type de média non compressé pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="22d3a-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d3a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22d3a-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="22d3a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22d3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d3a-109">*PMT* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="22d3a-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22d3a-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui est remplie avec le type de média.</span><span class="sxs-lookup"><span data-stu-id="22d3a-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d3a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22d3a-111">Return value</span></span>

<span data-ttu-id="22d3a-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="22d3a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="22d3a-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22d3a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d3a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="22d3a-114">Remarks</span></span>

<span data-ttu-id="22d3a-115">L’appelant doit libérer le bloc de format du type de média retourné, fourni dans le membre **pbFormat** de la structure de type de média am retournée \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="22d3a-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="22d3a-116">Vous pouvez utiliser la fonction d’assistance [**FreeMediaType**](freemediatype.md) à partir de la bibliothèque de classes de base.</span><span class="sxs-lookup"><span data-stu-id="22d3a-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="22d3a-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="22d3a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="22d3a-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="22d3a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="22d3a-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="22d3a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22d3a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22d3a-120">Requirements</span></span>



| <span data-ttu-id="22d3a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22d3a-121">Requirement</span></span> | <span data-ttu-id="22d3a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="22d3a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22d3a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="22d3a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="22d3a-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="22d3a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="22d3a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22d3a-125">Library</span></span><br/> | <dl> <span data-ttu-id="22d3a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22d3a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d3a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22d3a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d3a-128">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="22d3a-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="22d3a-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="22d3a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




