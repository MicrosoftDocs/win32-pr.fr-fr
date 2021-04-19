---
description: La méthode Remove supprime cet objet de la chronologie (y compris les sous-objets, mais pas les enfants), à des fins de réinsertion ailleurs.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: 'IAMTimelineObj :: Remove, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a3559787dfdacc68130dcaef073f32d07d4a0df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528817"
---
# <a name="iamtimelineobjremove-method"></a><span data-ttu-id="014c4-103">IAMTimelineObj :: Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="014c4-103">IAMTimelineObj::Remove method</span></span>

> [!Note]  
> <span data-ttu-id="014c4-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="014c4-104">\[Deprecated.</span></span> <span data-ttu-id="014c4-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="014c4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="014c4-106">La `Remove` méthode supprime cet objet de la chronologie (y compris les sous-objets, mais pas les enfants), à des fins de réinsertion ailleurs.</span><span class="sxs-lookup"><span data-stu-id="014c4-106">The `Remove` method removes this object from the timeline (including subobjects but not children), for reinsertion elsewhere.</span></span>

## <a name="syntax"></a><span data-ttu-id="014c4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="014c4-107">Syntax</span></span>


```C++
HRESULT Remove();
```



## <a name="parameters"></a><span data-ttu-id="014c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="014c4-108">Parameters</span></span>

<span data-ttu-id="014c4-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="014c4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="014c4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="014c4-110">Return value</span></span>

<span data-ttu-id="014c4-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="014c4-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="014c4-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="014c4-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="014c4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="014c4-113">Remarks</span></span>

<span data-ttu-id="014c4-114">Appelez cette méthode uniquement si l’application Insère immédiatement l’objet dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="014c4-114">Call this method only if the application will immediately insert the object back into the timeline.</span></span> <span data-ttu-id="014c4-115">Il s’agit d’une opération non valide pour appeler cette méthode sans réinsérer l’objet.</span><span class="sxs-lookup"><span data-stu-id="014c4-115">It is an invalid operation to call this method without then reinserting the object.</span></span> <span data-ttu-id="014c4-116">Pour supprimer définitivement un objet, appelez [**IAMTimelineObj :: RemoveAll**](iamtimelineobj-removeall.md).</span><span class="sxs-lookup"><span data-stu-id="014c4-116">To remove an object permanently, call [**IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).</span></span>

> [!Note]  
> <span data-ttu-id="014c4-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="014c4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="014c4-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="014c4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="014c4-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="014c4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="014c4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="014c4-120">Requirements</span></span>



| <span data-ttu-id="014c4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="014c4-121">Requirement</span></span> | <span data-ttu-id="014c4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="014c4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="014c4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="014c4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="014c4-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="014c4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="014c4-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="014c4-125">Library</span></span><br/> | <dl> <span data-ttu-id="014c4-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="014c4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014c4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="014c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014c4-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="014c4-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="014c4-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="014c4-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




