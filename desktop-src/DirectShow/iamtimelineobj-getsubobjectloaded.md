---
description: La méthode GetSubObjectLoaded détermine si le pointeur de sous-objet a été défini.
ms.assetid: 05b58435-eeca-4b52-9a53-ad7f81b5b35d
title: 'IAMTimelineObj :: GetSubObjectLoaded, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectLoaded
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 073810b6c02997d78e21a66976954d88e47ae82b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542295"
---
# <a name="iamtimelineobjgetsubobjectloaded-method"></a><span data-ttu-id="781d0-103">IAMTimelineObj :: GetSubObjectLoaded, méthode</span><span class="sxs-lookup"><span data-stu-id="781d0-103">IAMTimelineObj::GetSubObjectLoaded method</span></span>

> [!Note]  
> <span data-ttu-id="781d0-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="781d0-104">\[Deprecated.</span></span> <span data-ttu-id="781d0-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="781d0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="781d0-106">La `GetSubObjectLoaded` méthode détermine si le pointeur de sous-objet a été défini.</span><span class="sxs-lookup"><span data-stu-id="781d0-106">The `GetSubObjectLoaded` method determines whether the subobject pointer has been set.</span></span>

## <a name="syntax"></a><span data-ttu-id="781d0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="781d0-107">Syntax</span></span>


```C++
HRESULT GetSubObjectLoaded(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="781d0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="781d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="781d0-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="781d0-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="781d0-110">Reçoit une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="781d0-110">Receives a Boolean value.</span></span> <span data-ttu-id="781d0-111">Si la valeur est **true**, le pointeur de sous-objet a été défini.</span><span class="sxs-lookup"><span data-stu-id="781d0-111">If the value is **TRUE**, the subobject pointer has been set.</span></span> <span data-ttu-id="781d0-112">Si la **valeur est false**, le pointeur n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="781d0-112">If **FALSE**, the pointer has not been set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="781d0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="781d0-113">Return value</span></span>

<span data-ttu-id="781d0-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="781d0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="781d0-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="781d0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="781d0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="781d0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="781d0-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="781d0-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="781d0-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="781d0-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="781d0-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="781d0-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="781d0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="781d0-120">Requirements</span></span>



| <span data-ttu-id="781d0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="781d0-121">Requirement</span></span> | <span data-ttu-id="781d0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="781d0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="781d0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="781d0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="781d0-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="781d0-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="781d0-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="781d0-125">Library</span></span><br/> | <dl> <span data-ttu-id="781d0-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="781d0-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781d0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="781d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781d0-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="781d0-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="781d0-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="781d0-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




