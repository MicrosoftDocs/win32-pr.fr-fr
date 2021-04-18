---
description: La méthode GetNextSrcEx récupère la source suivante après la source spécifiée.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'IAMTimelineTrack :: GetNextSrcEx, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525992"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="4ddb8-103">IAMTimelineTrack :: GetNextSrcEx, méthode</span><span class="sxs-lookup"><span data-stu-id="4ddb8-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="4ddb8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-104">\[Deprecated.</span></span> <span data-ttu-id="4ddb8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ddb8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4ddb8-106">La `GetNextSrcEx` méthode récupère la source suivante après la source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddb8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ddb8-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="4ddb8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ddb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddb8-109">*pLast*</span><span class="sxs-lookup"><span data-stu-id="4ddb8-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddb8-110">Pointeur vers l’objet source précédent, ou **null** pour récupérer la première source dans la piste.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="4ddb8-111">*ppNext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4ddb8-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ddb8-112">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source suivant.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ddb8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ddb8-113">Return value</span></span>

<span data-ttu-id="4ddb8-114">Retourne \_ la valeur OK si la méthode récupère une source, ou la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ddb8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4ddb8-115">Remarks</span></span>

<span data-ttu-id="4ddb8-116">Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="4ddb8-117">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="4ddb8-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4ddb8-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ddb8-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4ddb8-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4ddb8-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ddb8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ddb8-121">Requirements</span></span>



| <span data-ttu-id="4ddb8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ddb8-122">Requirement</span></span> | <span data-ttu-id="4ddb8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ddb8-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ddb8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ddb8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4ddb8-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ddb8-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4ddb8-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ddb8-126">Library</span></span><br/> | <dl> <span data-ttu-id="4ddb8-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ddb8-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ddb8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ddb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ddb8-129">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="4ddb8-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="4ddb8-130">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="4ddb8-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




