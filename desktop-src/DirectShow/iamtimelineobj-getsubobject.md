---
description: La méthode GetSubObject récupère le sous-objet associé à cet objet.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'IAMTimelineObj :: GetSubObject, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542362"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="1a6ac-103">IAMTimelineObj :: GetSubObject, méthode</span><span class="sxs-lookup"><span data-stu-id="1a6ac-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="1a6ac-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-104">\[Deprecated.</span></span> <span data-ttu-id="1a6ac-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a6ac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a6ac-106">La `GetSubObject` méthode récupère le sous-objet associé à cet objet.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6ac-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a6ac-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1a6ac-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a6ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6ac-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1a6ac-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1a6ac-110">Reçoit un pointeur vers l’interface **IUnknown** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="1a6ac-111">Si l’objet n’a pas de sous-objet, la valeur est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6ac-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a6ac-112">Return value</span></span>

<span data-ttu-id="1a6ac-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a6ac-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a6ac-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6ac-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1a6ac-115">Remarks</span></span>

<span data-ttu-id="1a6ac-116">Chaque objet Timeline peut contenir un pointeur vers un sous-objet associé.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="1a6ac-117">Si la valeur retournée dans *pval* n’est pas **null**, l’interface **IUnknown** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="1a6ac-118">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="1a6ac-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a6ac-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a6ac-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a6ac-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a6ac-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a6ac-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a6ac-122">Requirements</span></span>



| <span data-ttu-id="1a6ac-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a6ac-123">Requirement</span></span> | <span data-ttu-id="1a6ac-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a6ac-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6ac-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a6ac-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1a6ac-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ac-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a6ac-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a6ac-127">Library</span></span><br/> | <dl> <span data-ttu-id="1a6ac-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a6ac-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6ac-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a6ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6ac-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="1a6ac-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="1a6ac-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="1a6ac-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




