---
description: La méthode SetSubObjectGUID spécifie le GUID du sous-objet associé à cet objet.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'IAMTimelineObj :: SetSubObjectGUID, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537799"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a><span data-ttu-id="b6867-103">IAMTimelineObj :: SetSubObjectGUID, méthode</span><span class="sxs-lookup"><span data-stu-id="b6867-103">IAMTimelineObj::SetSubObjectGUID method</span></span>

> [!Note]  
> <span data-ttu-id="b6867-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b6867-104">\[Deprecated.</span></span> <span data-ttu-id="b6867-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6867-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b6867-106">La `SetSubObjectGUID` méthode spécifie le GUID du sous-objet associé à cet objet.</span><span class="sxs-lookup"><span data-stu-id="b6867-106">The `SetSubObjectGUID` method specifies the GUID of the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6867-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6867-107">Syntax</span></span>


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b6867-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6867-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6867-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="b6867-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b6867-110">GUID du sous-objet.</span><span class="sxs-lookup"><span data-stu-id="b6867-110">GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6867-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6867-111">Return value</span></span>

<span data-ttu-id="b6867-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b6867-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b6867-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6867-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6867-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b6867-114">Remarks</span></span>

<span data-ttu-id="b6867-115">Le moteur de rendu crée une instance du sous-objet en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="b6867-115">The render engine creates an instance of the subobject as needed.</span></span>

> [!Note]  
> <span data-ttu-id="b6867-116">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b6867-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b6867-117">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6867-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b6867-118">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b6867-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6867-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6867-119">Requirements</span></span>



| <span data-ttu-id="b6867-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6867-120">Requirement</span></span> | <span data-ttu-id="b6867-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6867-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6867-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6867-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b6867-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6867-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b6867-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6867-124">Library</span></span><br/> | <dl> <span data-ttu-id="b6867-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6867-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6867-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6867-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6867-127">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b6867-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b6867-128">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b6867-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




