---
description: 'IAMTimeline :: IsDirty, méthode-non pris en charge.'
ms.assetid: ed6fd633-23b8-4b80-901c-d7b50fa4c15e
title: 'IAMTimeline :: IsDirty, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.IsDirty
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ee51c44ae99a26e54a616da6752511f8a4e5f4a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119587"
---
# <a name="iamtimelineisdirty-method"></a><span data-ttu-id="72dfa-103">IAMTimeline :: IsDirty, méthode</span><span class="sxs-lookup"><span data-stu-id="72dfa-103">IAMTimeline::IsDirty method</span></span>

> [!Note]  
> <span data-ttu-id="72dfa-104">\[Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="72dfa-104">\[Deprecated.</span></span> <span data-ttu-id="72dfa-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72dfa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72dfa-106">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="72dfa-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="72dfa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72dfa-107">Syntax</span></span>


```C++
HRESULT IsDirty(
   BOOL *pDirty
);
```



## <a name="parameters"></a><span data-ttu-id="72dfa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72dfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72dfa-109">*pDirty*</span><span class="sxs-lookup"><span data-stu-id="72dfa-109">*pDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="72dfa-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="72dfa-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72dfa-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="72dfa-111">Return value</span></span>

<span data-ttu-id="72dfa-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72dfa-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72dfa-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72dfa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72dfa-114">Notes </span><span class="sxs-lookup"><span data-stu-id="72dfa-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72dfa-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="72dfa-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72dfa-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72dfa-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72dfa-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="72dfa-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72dfa-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72dfa-118">Requirements</span></span>



| <span data-ttu-id="72dfa-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72dfa-119">Requirement</span></span> | <span data-ttu-id="72dfa-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="72dfa-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72dfa-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="72dfa-121">Header</span></span><br/>  | <dl> <span data-ttu-id="72dfa-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="72dfa-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72dfa-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72dfa-123">Library</span></span><br/> | <dl> <span data-ttu-id="72dfa-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72dfa-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72dfa-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72dfa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72dfa-126">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="72dfa-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




