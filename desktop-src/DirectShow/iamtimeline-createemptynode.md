---
description: La méthode CreateEmptyNode crée un nouvel objet Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'IAMTimeline :: CreateEmptyNode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528695"
---
# <a name="iamtimelinecreateemptynode-method"></a><span data-ttu-id="925ff-103">IAMTimeline :: CreateEmptyNode, méthode</span><span class="sxs-lookup"><span data-stu-id="925ff-103">IAMTimeline::CreateEmptyNode method</span></span>

> [!Note]  
> <span data-ttu-id="925ff-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="925ff-104">\[Deprecated.</span></span> <span data-ttu-id="925ff-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="925ff-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="925ff-106">La `CreateEmptyNode` méthode crée un nouvel objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="925ff-106">The `CreateEmptyNode` method creates a new timeline object.</span></span>

<span data-ttu-id="925ff-107">Utilisez cette méthode pour créer des objets Timeline, plutôt que la fonction **CoCreateInstance** , car cette méthode exécute des routines d’initialisation importantes.</span><span class="sxs-lookup"><span data-stu-id="925ff-107">Use this method to create timeline objects, rather than the **CoCreateInstance** function, because this method performs important initialization routines.</span></span> <span data-ttu-id="925ff-108">Chaque objet créé par cette méthode prend en charge au moins l’interface [**IAMTimelineObj**](iamtimelineobj.md) , ainsi que d’autres interfaces spécifiques à ce type d’objet.</span><span class="sxs-lookup"><span data-stu-id="925ff-108">Every object created by this method supports at least the [**IAMTimelineObj**](iamtimelineobj.md) interface, along with other interfaces specific to that type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="925ff-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="925ff-109">Syntax</span></span>


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="925ff-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="925ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925ff-111">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="925ff-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="925ff-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) du nouvel objet.</span><span class="sxs-lookup"><span data-stu-id="925ff-112">Receives a pointer to the new object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="925ff-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="925ff-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="925ff-114">Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) , en spécifiant le type d’objet à créer.</span><span class="sxs-lookup"><span data-stu-id="925ff-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925ff-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="925ff-115">Return value</span></span>

<span data-ttu-id="925ff-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="925ff-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="925ff-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="925ff-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="925ff-118">Notes</span><span class="sxs-lookup"><span data-stu-id="925ff-118">Remarks</span></span>

<span data-ttu-id="925ff-119">N’ajoutez pas le nouvel objet à une autre instance de chronologie.</span><span class="sxs-lookup"><span data-stu-id="925ff-119">Do not add the new object to another timeline instance.</span></span> <span data-ttu-id="925ff-120">Chaque objet d’une chronologie doit être créé par cette chronologie.</span><span class="sxs-lookup"><span data-stu-id="925ff-120">Every object in a timeline must be created by that timeline.</span></span>

<span data-ttu-id="925ff-121">Si la méthode est réussie, l’interface [**IAMTimelineObj**](iamtimelineobj.md) qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="925ff-121">If the method succeeds, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="925ff-122">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="925ff-122">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="925ff-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="925ff-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="925ff-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="925ff-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="925ff-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="925ff-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="925ff-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="925ff-126">Requirements</span></span>



| <span data-ttu-id="925ff-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="925ff-127">Requirement</span></span> | <span data-ttu-id="925ff-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="925ff-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="925ff-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="925ff-129">Header</span></span><br/>  | <dl> <span data-ttu-id="925ff-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="925ff-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="925ff-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="925ff-131">Library</span></span><br/> | <dl> <span data-ttu-id="925ff-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="925ff-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="925ff-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="925ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925ff-134">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="925ff-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="925ff-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="925ff-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




