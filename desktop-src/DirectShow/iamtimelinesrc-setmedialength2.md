---
description: 'La méthode SetMediaLength2 spécifie la durée du fichier source. Cette méthode est équivalente à IAMTimelineSrc :: SetMediaLength, mais prend une valeur REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'IAMTimelineSrc :: SetMediaLength2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526769"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a><span data-ttu-id="34275-104">IAMTimelineSrc :: SetMediaLength2, méthode</span><span class="sxs-lookup"><span data-stu-id="34275-104">IAMTimelineSrc::SetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="34275-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="34275-105">\[Deprecated.</span></span> <span data-ttu-id="34275-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="34275-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="34275-107">La `SetMediaLength2` méthode spécifie la durée du fichier source.</span><span class="sxs-lookup"><span data-stu-id="34275-107">The `SetMediaLength2` method specifies the duration of the source file.</span></span> <span data-ttu-id="34275-108">Cette méthode est équivalente à [**IAMTimelineSrc :: SetMediaLength**](iamtimelinesrc-setmedialength.md), mais prend une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="34275-108">This method is equivalent to [**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="34275-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34275-109">Syntax</span></span>


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="34275-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34275-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34275-111">*Durée*</span><span class="sxs-lookup"><span data-stu-id="34275-111">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="34275-112">Longueur du média, en secondes.</span><span class="sxs-lookup"><span data-stu-id="34275-112">Media length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34275-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34275-113">Return value</span></span>

<span data-ttu-id="34275-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="34275-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34275-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34275-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34275-116">Notes</span><span class="sxs-lookup"><span data-stu-id="34275-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="34275-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="34275-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="34275-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="34275-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="34275-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="34275-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34275-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34275-120">Requirements</span></span>



| <span data-ttu-id="34275-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34275-121">Requirement</span></span> | <span data-ttu-id="34275-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="34275-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34275-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="34275-123">Header</span></span><br/>  | <dl> <span data-ttu-id="34275-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="34275-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="34275-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34275-125">Library</span></span><br/> | <dl> <span data-ttu-id="34275-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34275-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34275-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34275-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34275-128">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="34275-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="34275-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="34275-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




