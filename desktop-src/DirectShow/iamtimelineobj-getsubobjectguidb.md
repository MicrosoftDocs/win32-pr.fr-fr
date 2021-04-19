---
description: 'La méthode GetSubObjectGUIDB récupère le GUID du sous-objet associé à cet objet Timeline. Cette méthode est équivalente à IAMTimelineObj :: GetSubObjectGUID, mais elle reçoit une valeur BSTR.'
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'IAMTimelineObj :: GetSubObjectGUIDB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530466"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="27907-104">IAMTimelineObj :: GetSubObjectGUIDB, méthode</span><span class="sxs-lookup"><span data-stu-id="27907-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="27907-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="27907-105">\[Deprecated.</span></span> <span data-ttu-id="27907-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27907-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27907-107">La `GetSubObjectGUIDB` méthode récupère le GUID du sous-objet associé à cet objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="27907-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="27907-108">Cette méthode est équivalente à [**IAMTimelineObj :: GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), mais elle reçoit une valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="27907-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="27907-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27907-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="27907-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27907-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27907-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27907-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27907-112">Reçoit une chaîne représentant le GUID de sous-objet.</span><span class="sxs-lookup"><span data-stu-id="27907-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27907-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27907-113">Return value</span></span>

<span data-ttu-id="27907-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27907-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27907-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27907-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27907-116">Notes</span><span class="sxs-lookup"><span data-stu-id="27907-116">Remarks</span></span>

<span data-ttu-id="27907-117">La méthode alloue de la mémoire pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="27907-117">The method allocates memory for the string.</span></span> <span data-ttu-id="27907-118">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="27907-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="27907-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="27907-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27907-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27907-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27907-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27907-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27907-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27907-122">Requirements</span></span>



| <span data-ttu-id="27907-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27907-123">Requirement</span></span> | <span data-ttu-id="27907-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="27907-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27907-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="27907-125">Header</span></span><br/>  | <dl> <span data-ttu-id="27907-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27907-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27907-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27907-127">Library</span></span><br/> | <dl> <span data-ttu-id="27907-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27907-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27907-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27907-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27907-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="27907-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="27907-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="27907-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




