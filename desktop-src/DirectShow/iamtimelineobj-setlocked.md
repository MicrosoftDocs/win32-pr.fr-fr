---
description: La méthode SetLocked définit l’état de modification de l’objet sur verrouillé ou déverrouillé.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'IAMTimelineObj :: SetLocked, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543269"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="17479-103">IAMTimelineObj :: SetLocked, méthode</span><span class="sxs-lookup"><span data-stu-id="17479-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="17479-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="17479-104">\[Deprecated.</span></span> <span data-ttu-id="17479-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17479-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17479-106">La `SetLocked` méthode définit l’état de modification de l’objet sur verrouillé ou déverrouillé.</span><span class="sxs-lookup"><span data-stu-id="17479-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="17479-107">Un état verrouillé indique que l’objet ne doit pas être modifié ; un État déverrouillé indique que l’objet peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="17479-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="17479-108">La chronologie n’applique pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="17479-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="17479-109">Le paramètre verrouillé existe uniquement pour la commodité de l’application.</span><span class="sxs-lookup"><span data-stu-id="17479-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="17479-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17479-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="17479-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17479-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17479-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="17479-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="17479-113">Valeur booléenne qui spécifie l’état de modification de l’objet.</span><span class="sxs-lookup"><span data-stu-id="17479-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="17479-114">Si la **valeur est true**, l’objet est verrouillé et ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="17479-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="17479-115">Si la **valeur est false**, l’objet est déverrouillé et peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="17479-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17479-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17479-116">Return value</span></span>

<span data-ttu-id="17479-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17479-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17479-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17479-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17479-119">Notes</span><span class="sxs-lookup"><span data-stu-id="17479-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="17479-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="17479-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17479-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="17479-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17479-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="17479-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17479-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17479-123">Requirements</span></span>



| <span data-ttu-id="17479-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17479-124">Requirement</span></span> | <span data-ttu-id="17479-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="17479-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17479-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="17479-126">Header</span></span><br/>  | <dl> <span data-ttu-id="17479-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="17479-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17479-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17479-128">Library</span></span><br/> | <dl> <span data-ttu-id="17479-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17479-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17479-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17479-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17479-131">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="17479-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="17479-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="17479-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




