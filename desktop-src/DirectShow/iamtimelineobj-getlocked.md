---
description: La méthode GetLocked récupère l’état d’édition de l’objet (verrouillé ou déverrouillé).
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'IAMTimelineObj :: GetLocked, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521674"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="c5ab7-103">IAMTimelineObj :: GetLocked, méthode</span><span class="sxs-lookup"><span data-stu-id="c5ab7-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="c5ab7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-104">\[Deprecated.</span></span> <span data-ttu-id="c5ab7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5ab7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c5ab7-106">La `GetLocked` méthode récupère l’état d’édition de l’objet (verrouillé ou déverrouillé).</span><span class="sxs-lookup"><span data-stu-id="c5ab7-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="c5ab7-107">Un état verrouillé indique que l’objet ne doit pas être modifié ; un État déverrouillé indique que l’objet peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="c5ab7-108">La chronologie n’applique pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="c5ab7-109">Le paramètre verrouillé existe uniquement pour la commodité de l’application.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ab7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5ab7-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c5ab7-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5ab7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ab7-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="c5ab7-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ab7-113">Reçoit l’état de modification de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-113">Receives the object's editing state.</span></span> <span data-ttu-id="c5ab7-114">Si la valeur est **true**, l’objet est verrouillé et ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="c5ab7-115">Si la **valeur est false**, l’objet est déverrouillé et peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5ab7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c5ab7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c5ab7-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c5ab7-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5ab7-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c5ab7-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c5ab7-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5ab7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5ab7-120">Requirements</span></span>



| <span data-ttu-id="c5ab7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5ab7-121">Requirement</span></span> | <span data-ttu-id="c5ab7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5ab7-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ab7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5ab7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c5ab7-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ab7-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c5ab7-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c5ab7-125">Library</span></span><br/> | <dl> <span data-ttu-id="c5ab7-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5ab7-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ab7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5ab7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ab7-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="c5ab7-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="c5ab7-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="c5ab7-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




