---
description: 'La méthode GetDefaultTransitionB récupère la transition par défaut. Cette méthode est équivalente à IAMTimeline :: GetDefaultTransition, mais elle reçoit une valeur BSTR plutôt qu’un GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'IAMTimeline :: GetDefaultTransitionB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535387"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a><span data-ttu-id="27def-104">IAMTimeline :: GetDefaultTransitionB, méthode</span><span class="sxs-lookup"><span data-stu-id="27def-104">IAMTimeline::GetDefaultTransitionB method</span></span>

> [!Note]  
> <span data-ttu-id="27def-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27def-105">\[Deprecated.</span></span> <span data-ttu-id="27def-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27def-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27def-107">La `GetDefaultTransitionB` méthode récupère la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="27def-107">The `GetDefaultTransitionB` method retrieves the default transition.</span></span> <span data-ttu-id="27def-108">Cette méthode est équivalente à [**IAMTimeline :: GetDefaultTransition**](iamtimeline-getdefaulttransition.md), mais elle reçoit une valeur BSTR plutôt qu’un GUID.</span><span class="sxs-lookup"><span data-stu-id="27def-108">This method is equivalent to [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), but receives a BSTR value, rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="27def-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27def-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="27def-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27def-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27def-111">*pguid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27def-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27def-112">Reçoit une valeur **BSTR** représentant le GUID de la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="27def-112">Receives a **BSTR** value representing the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27def-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27def-113">Return value</span></span>

<span data-ttu-id="27def-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27def-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27def-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27def-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27def-116">Notes</span><span class="sxs-lookup"><span data-stu-id="27def-116">Remarks</span></span>

<span data-ttu-id="27def-117">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="27def-117">The method allocates memory for the string.</span></span> <span data-ttu-id="27def-118">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="27def-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="27def-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="27def-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27def-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27def-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27def-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27def-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27def-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27def-122">Requirements</span></span>



| <span data-ttu-id="27def-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27def-123">Requirement</span></span> | <span data-ttu-id="27def-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="27def-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27def-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="27def-125">Header</span></span><br/>  | <dl> <span data-ttu-id="27def-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27def-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27def-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27def-127">Library</span></span><br/> | <dl> <span data-ttu-id="27def-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27def-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27def-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27def-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27def-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="27def-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="27def-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="27def-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




