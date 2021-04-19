---
description: La méthode SetUserID définit un identificateur défini par l’application pour l’objet.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: 'IAMTimelineObj :: SetUserID, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 31a0c59c6c93535be1200b2cd7678d4c355b5bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525563"
---
# <a name="iamtimelineobjsetuserid-method"></a><span data-ttu-id="4c6d9-103">IAMTimelineObj :: SetUserID, méthode</span><span class="sxs-lookup"><span data-stu-id="4c6d9-103">IAMTimelineObj::SetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="4c6d9-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-104">\[Deprecated.</span></span> <span data-ttu-id="4c6d9-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c6d9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c6d9-106">La `SetUserID` méthode définit un identificateur défini par l’application pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-106">The `SetUserID` method sets an application-defined identifier for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c6d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c6d9-107">Syntax</span></span>


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4c6d9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c6d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c6d9-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="4c6d9-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="4c6d9-110">Valeur qui spécifie l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-110">Value that specifies the identifier.</span></span> <span data-ttu-id="4c6d9-111">Cet identificateur est utilisé uniquement par l’application et peut être n’importe quelle valeur.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-111">This identifier is used only by the application and can be any value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c6d9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c6d9-112">Return value</span></span>

<span data-ttu-id="4c6d9-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c6d9-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c6d9-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c6d9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4c6d9-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c6d9-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c6d9-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c6d9-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c6d9-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4c6d9-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c6d9-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c6d9-119">Requirements</span></span>



| <span data-ttu-id="4c6d9-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c6d9-120">Requirement</span></span> | <span data-ttu-id="4c6d9-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c6d9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6d9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c6d9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4c6d9-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c6d9-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c6d9-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4c6d9-124">Library</span></span><br/> | <dl> <span data-ttu-id="4c6d9-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c6d9-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c6d9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c6d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c6d9-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="4c6d9-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4c6d9-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="4c6d9-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




