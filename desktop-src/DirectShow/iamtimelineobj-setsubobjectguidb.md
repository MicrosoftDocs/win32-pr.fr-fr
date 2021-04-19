---
description: 'La méthode SetSubObjectGUIDB spécifie le GUID du sous-objet associé à cet objet. Cette méthode est équivalente à IAMTimelineObj :: SetSubObjectGUID, mais prend une valeur BSTR.'
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'IAMTimelineObj :: SetSubObjectGUIDB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533050"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="1203d-104">IAMTimelineObj :: SetSubObjectGUIDB, méthode</span><span class="sxs-lookup"><span data-stu-id="1203d-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="1203d-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1203d-105">\[Deprecated.</span></span> <span data-ttu-id="1203d-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1203d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1203d-107">La `SetSubObjectGUIDB` méthode spécifie le GUID du sous-objet associé à cet objet.</span><span class="sxs-lookup"><span data-stu-id="1203d-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="1203d-108">Cette méthode est équivalente à [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) , mais prend une valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="1203d-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1203d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1203d-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="1203d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1203d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1203d-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="1203d-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="1203d-112">**BSTR** représentant le GUID du sous-objet.</span><span class="sxs-lookup"><span data-stu-id="1203d-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1203d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1203d-113">Return value</span></span>

<span data-ttu-id="1203d-114">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1203d-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1203d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1203d-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1203d-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="1203d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1203d-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1203d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1203d-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1203d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1203d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1203d-119">Requirements</span></span>



| <span data-ttu-id="1203d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1203d-120">Requirement</span></span> | <span data-ttu-id="1203d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1203d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1203d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1203d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1203d-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1203d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1203d-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1203d-124">Library</span></span><br/> | <dl> <span data-ttu-id="1203d-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1203d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1203d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1203d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1203d-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="1203d-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="1203d-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="1203d-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




