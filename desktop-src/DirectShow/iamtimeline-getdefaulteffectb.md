---
description: 'La méthode GetDefaultEffectB récupère l’effet par défaut. Cette méthode est équivalente à IAMTimeline :: GetDefaultEffect, mais elle reçoit une valeur BSTR plutôt qu’un GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'IAMTimeline :: GetDefaultEffectB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521669"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a><span data-ttu-id="5bb86-104">IAMTimeline :: GetDefaultEffectB, méthode</span><span class="sxs-lookup"><span data-stu-id="5bb86-104">IAMTimeline::GetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="5bb86-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5bb86-105">\[Deprecated.</span></span> <span data-ttu-id="5bb86-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5bb86-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5bb86-107">La `GetDefaultEffectB` méthode récupère l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="5bb86-107">The `GetDefaultEffectB` method retrieves the default effect.</span></span> <span data-ttu-id="5bb86-108">Cette méthode est équivalente à [**IAMTimeline :: GetDefaultEffect**](iamtimeline-getdefaulteffect.md), mais elle reçoit une valeur **BSTR** plutôt qu’un GUID.</span><span class="sxs-lookup"><span data-stu-id="5bb86-108">This method is equivalent to [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), but receives a **BSTR** value rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb86-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bb86-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="5bb86-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bb86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb86-111">*pguid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5bb86-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb86-112">Reçoit une valeur **BSTR** représentant le GUID de l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="5bb86-112">Receives a **BSTR** value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb86-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bb86-113">Return value</span></span>

<span data-ttu-id="5bb86-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5bb86-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5bb86-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5bb86-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bb86-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5bb86-116">Remarks</span></span>

<span data-ttu-id="5bb86-117">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5bb86-117">The method allocates memory for the string.</span></span> <span data-ttu-id="5bb86-118">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5bb86-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="5bb86-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5bb86-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5bb86-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5bb86-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5bb86-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5bb86-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5bb86-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bb86-122">Requirements</span></span>



| <span data-ttu-id="5bb86-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bb86-123">Requirement</span></span> | <span data-ttu-id="5bb86-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bb86-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb86-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bb86-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5bb86-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bb86-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5bb86-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5bb86-127">Library</span></span><br/> | <dl> <span data-ttu-id="5bb86-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bb86-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb86-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bb86-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb86-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="5bb86-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="5bb86-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="5bb86-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




