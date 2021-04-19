---
description: La méthode SetMuted définit l’État muet de l’objet. Un objet muet n’est pas rendu, mais il reste dans la chronologie.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'IAMTimelineObj :: SetMuted, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534808"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="f26b3-104">IAMTimelineObj :: SetMuted, méthode</span><span class="sxs-lookup"><span data-stu-id="f26b3-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="f26b3-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f26b3-105">\[Deprecated.</span></span> <span data-ttu-id="f26b3-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f26b3-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f26b3-107">La `SetMuted` méthode définit l’État muet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f26b3-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="f26b3-108">Un objet muet n’est pas rendu, mais il reste dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="f26b3-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="f26b3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f26b3-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="f26b3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f26b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f26b3-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="f26b3-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f26b3-112">Indicateur qui spécifie l’État muet.</span><span class="sxs-lookup"><span data-stu-id="f26b3-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="f26b3-113">Si la **valeur est true**, l’objet et tous ses enfants sont muets.</span><span class="sxs-lookup"><span data-stu-id="f26b3-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f26b3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f26b3-114">Return value</span></span>

<span data-ttu-id="f26b3-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f26b3-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f26b3-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f26b3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f26b3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f26b3-117">Remarks</span></span>

<span data-ttu-id="f26b3-118">La désactivation d’un objet désactive également tous les enfants contenus dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="f26b3-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="f26b3-119">Par exemple, si vous désactivez une piste, les transitions, les sources et les effets de cette piste sont également muets.</span><span class="sxs-lookup"><span data-stu-id="f26b3-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="f26b3-120">Une fois que l’objet n’est plus muet, ses enfants reviennent à leur état précédent, qui peut être muet ou muet.</span><span class="sxs-lookup"><span data-stu-id="f26b3-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="f26b3-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f26b3-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f26b3-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f26b3-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f26b3-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f26b3-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f26b3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f26b3-124">Requirements</span></span>



| <span data-ttu-id="f26b3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f26b3-125">Requirement</span></span> | <span data-ttu-id="f26b3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f26b3-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f26b3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f26b3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f26b3-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f26b3-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f26b3-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f26b3-129">Library</span></span><br/> | <dl> <span data-ttu-id="f26b3-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f26b3-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f26b3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f26b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26b3-132">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f26b3-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f26b3-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="f26b3-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




