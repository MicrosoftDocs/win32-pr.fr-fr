---
description: La méthode GetUserID récupère l’identificateur défini par l’application de l’objet.
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: 'IAMTimelineObj :: GetUserID, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f5d6c07fd826f2045ddc9f54445bc96feb5a7c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538570"
---
# <a name="iamtimelineobjgetuserid-method"></a><span data-ttu-id="6a374-103">IAMTimelineObj :: GetUserID, méthode</span><span class="sxs-lookup"><span data-stu-id="6a374-103">IAMTimelineObj::GetUserID method</span></span>

> [!Note]  
> <span data-ttu-id="6a374-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="6a374-104">\[Deprecated.</span></span> <span data-ttu-id="6a374-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a374-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6a374-106">La `GetUserID` méthode récupère l’identificateur défini par l’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6a374-106">The `GetUserID` method retrieves the object's application-defined identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a374-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a374-107">Syntax</span></span>


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6a374-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a374-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a374-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="6a374-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="6a374-110">Reçoit l’identificateur défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="6a374-110">Receives the application-defined identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a374-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a374-111">Return value</span></span>

<span data-ttu-id="6a374-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a374-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a374-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a374-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a374-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6a374-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a374-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="6a374-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6a374-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6a374-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6a374-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6a374-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a374-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a374-118">Requirements</span></span>



| <span data-ttu-id="6a374-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a374-119">Requirement</span></span> | <span data-ttu-id="6a374-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a374-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a374-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a374-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6a374-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a374-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6a374-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a374-123">Library</span></span><br/> | <dl> <span data-ttu-id="6a374-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a374-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a374-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a374-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a374-126">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="6a374-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6a374-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="6a374-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




