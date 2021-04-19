---
description: La \_ méthode d’extraction de MediaType retourne le type de média de sortie actuel du filtre de redimensionnement.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'IResize :: get_MediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542749"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="2da46-103">IResize :: obtient la \_ méthode MediaType</span><span class="sxs-lookup"><span data-stu-id="2da46-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="2da46-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2da46-104">\[Deprecated.</span></span> <span data-ttu-id="2da46-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2da46-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2da46-106">La `get_MediaType` méthode retourne le type de média de sortie actuel du filtre de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="2da46-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da46-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2da46-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="2da46-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2da46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da46-109">*PMT* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2da46-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2da46-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="2da46-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="2da46-111">La méthode remplit cette structure avec le type de média.</span><span class="sxs-lookup"><span data-stu-id="2da46-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="2da46-112">L’appelant doit libérer le bloc de format, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2da46-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da46-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2da46-113">Return value</span></span>

<span data-ttu-id="2da46-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2da46-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2da46-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2da46-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da46-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2da46-116">Remarks</span></span>

<span data-ttu-id="2da46-117">Si le type de média de sortie n’a pas été défini, retourne un type de média par défaut.</span><span class="sxs-lookup"><span data-stu-id="2da46-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="2da46-118">Le filtre doit mettre à jour son type de média de sortie lorsque les méthodes **put \_ MediaType** ou **put \_ Size** sont appelées ; le type de média retourné par `get_MediaType` doit refléter ces modifications.</span><span class="sxs-lookup"><span data-stu-id="2da46-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="2da46-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="2da46-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2da46-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2da46-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2da46-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2da46-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2da46-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2da46-122">Requirements</span></span>



| <span data-ttu-id="2da46-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2da46-123">Requirement</span></span> | <span data-ttu-id="2da46-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="2da46-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da46-125">Version</span><span class="sxs-lookup"><span data-stu-id="2da46-125">Version</span></span><br/> | <span data-ttu-id="2da46-126">DirectX 9,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2da46-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="2da46-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2da46-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2da46-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da46-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2da46-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2da46-129">Library</span></span><br/> | <dl> <span data-ttu-id="2da46-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2da46-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da46-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2da46-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da46-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="2da46-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="2da46-133">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="2da46-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




