---
description: La méthode GetGenID récupère l’identificateur généré de l’objet. L’identificateur est un nombre réservé ; les applications ne doivent pas l’utiliser.
ms.assetid: b71b9b52-589b-4f80-915f-4805b1b8e295
title: 'IAMTimelineObj :: GetGenID, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetGenID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3497777d25c9a81d4334f1979ce33f351111ed4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541438"
---
# <a name="iamtimelineobjgetgenid-method"></a><span data-ttu-id="0b7a6-104">IAMTimelineObj :: GetGenID, méthode</span><span class="sxs-lookup"><span data-stu-id="0b7a6-104">IAMTimelineObj::GetGenID method</span></span>

> [!Note]  
> <span data-ttu-id="0b7a6-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-105">\[Deprecated.</span></span> <span data-ttu-id="0b7a6-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0b7a6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0b7a6-107">La `GetGenID` méthode récupère l’identificateur généré de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-107">The `GetGenID` method retrieves the object's generated identifier.</span></span> <span data-ttu-id="0b7a6-108">L’identificateur est un nombre réservé ; les applications ne doivent pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-108">The identifier is a reserved number; applications should not use it.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7a6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b7a6-109">Syntax</span></span>


```C++
HRESULT GetGenID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0b7a6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b7a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7a6-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="0b7a6-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7a6-112">Reçoit l’identificateur généré.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-112">Receives the generated identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b7a6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b7a6-113">Return value</span></span>

<span data-ttu-id="0b7a6-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b7a6-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b7a6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b7a6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0b7a6-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b7a6-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0b7a6-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b7a6-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0b7a6-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0b7a6-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b7a6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b7a6-120">Requirements</span></span>



| <span data-ttu-id="0b7a6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b7a6-121">Requirement</span></span> | <span data-ttu-id="0b7a6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b7a6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7a6-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b7a6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0b7a6-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b7a6-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0b7a6-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0b7a6-125">Library</span></span><br/> | <dl> <span data-ttu-id="0b7a6-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b7a6-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b7a6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b7a6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7a6-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="0b7a6-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="0b7a6-129">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0b7a6-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




