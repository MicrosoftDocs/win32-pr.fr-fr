---
description: La méthode GetMuted récupère l’État muet de l’objet.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'IAMTimelineObj :: GetMuted, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534826"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="2c265-103">IAMTimelineObj :: GetMuted, méthode</span><span class="sxs-lookup"><span data-stu-id="2c265-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="2c265-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2c265-104">\[Deprecated.</span></span> <span data-ttu-id="2c265-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2c265-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2c265-106">La `GetMuted` méthode récupère l’État muet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2c265-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c265-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c265-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2c265-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c265-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c265-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="2c265-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="2c265-110">Reçoit une valeur indiquant l’État muet.</span><span class="sxs-lookup"><span data-stu-id="2c265-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="2c265-111">Si la valeur est **true**, l’objet et ses enfants sont muets.</span><span class="sxs-lookup"><span data-stu-id="2c265-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c265-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c265-112">Return value</span></span>

<span data-ttu-id="2c265-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2c265-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c265-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c265-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c265-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2c265-115">Remarks</span></span>

<span data-ttu-id="2c265-116">Si le parent d’un objet est muet, l’objet est muet, quel que soit son état muet.</span><span class="sxs-lookup"><span data-stu-id="2c265-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="2c265-117">Lorsque le parent n’est plus muet, l’État muet précédent de l’objet est restauré.</span><span class="sxs-lookup"><span data-stu-id="2c265-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="2c265-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="2c265-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2c265-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c265-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2c265-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2c265-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c265-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c265-121">Requirements</span></span>



| <span data-ttu-id="2c265-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c265-122">Requirement</span></span> | <span data-ttu-id="2c265-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c265-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c265-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c265-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2c265-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c265-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2c265-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c265-126">Library</span></span><br/> | <dl> <span data-ttu-id="2c265-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c265-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c265-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c265-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c265-129">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="2c265-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="2c265-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="2c265-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




