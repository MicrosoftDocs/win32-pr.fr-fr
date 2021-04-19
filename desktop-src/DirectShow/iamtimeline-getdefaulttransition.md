---
description: La méthode GetDefaultTransition récupère la transition par défaut. Si le moteur de rendu ne peut pas restituer une transition, il remplace la transition par défaut.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'IAMTimeline :: GetDefaultTransition, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541666"
---
# <a name="iamtimelinegetdefaulttransition-method"></a><span data-ttu-id="fa480-104">IAMTimeline :: GetDefaultTransition, méthode</span><span class="sxs-lookup"><span data-stu-id="fa480-104">IAMTimeline::GetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="fa480-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fa480-105">\[Deprecated.</span></span> <span data-ttu-id="fa480-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa480-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa480-107">La `GetDefaultTransition` méthode récupère la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa480-107">The `GetDefaultTransition` method retrieves the default transition.</span></span> <span data-ttu-id="fa480-108">Si le moteur de rendu ne peut pas restituer une transition, il remplace la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa480-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa480-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa480-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="fa480-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa480-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa480-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="fa480-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="fa480-112">Reçoit le GUID de la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa480-112">Receives the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa480-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa480-113">Return value</span></span>

<span data-ttu-id="fa480-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa480-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa480-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa480-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa480-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fa480-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa480-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="fa480-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa480-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa480-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa480-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fa480-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa480-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa480-120">Requirements</span></span>



| <span data-ttu-id="fa480-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa480-121">Requirement</span></span> | <span data-ttu-id="fa480-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa480-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa480-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa480-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fa480-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa480-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa480-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa480-125">Library</span></span><br/> | <dl> <span data-ttu-id="fa480-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa480-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa480-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa480-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa480-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="fa480-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="fa480-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="fa480-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




