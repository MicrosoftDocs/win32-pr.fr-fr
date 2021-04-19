---
description: La méthode RemoveAll supprime définitivement cet objet de la chronologie, y compris les sous-objets et les enfants.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'IAMTimelineObj :: RemoveAll, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538137"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="27e0b-103">IAMTimelineObj :: RemoveAll, méthode</span><span class="sxs-lookup"><span data-stu-id="27e0b-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="27e0b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27e0b-104">\[Deprecated.</span></span> <span data-ttu-id="27e0b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27e0b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27e0b-106">La `RemoveAll` méthode supprime définitivement cet objet de la chronologie, y compris les sous-objets et les enfants.</span><span class="sxs-lookup"><span data-stu-id="27e0b-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e0b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27e0b-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="27e0b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27e0b-108">Parameters</span></span>

<span data-ttu-id="27e0b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="27e0b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27e0b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27e0b-110">Return value</span></span>

<span data-ttu-id="27e0b-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27e0b-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27e0b-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27e0b-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27e0b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="27e0b-113">Remarks</span></span>

<span data-ttu-id="27e0b-114">Pour supprimer un objet en vue de le réinsérer ailleurs dans la chronologie, appelez [**IAMTimelineObj :: Remove**](iamtimelineobj-remove.md).</span><span class="sxs-lookup"><span data-stu-id="27e0b-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="27e0b-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="27e0b-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27e0b-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27e0b-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27e0b-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27e0b-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27e0b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27e0b-118">Requirements</span></span>



| <span data-ttu-id="27e0b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27e0b-119">Requirement</span></span> | <span data-ttu-id="27e0b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="27e0b-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27e0b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="27e0b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="27e0b-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27e0b-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27e0b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27e0b-123">Library</span></span><br/> | <dl> <span data-ttu-id="27e0b-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27e0b-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e0b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27e0b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e0b-126">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="27e0b-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="27e0b-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="27e0b-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




