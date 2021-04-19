---
description: La méthode GetPropertySetter récupère l’accesseur Set de la propriété de l’objet. Lorsque l’objet est rendu, les informations de propriété contenues dans l’accesseur Set de propriété sont appliquées à l’objet.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'IAMTimelineObj :: GetPropertySetter, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541676"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="2e2b0-104">IAMTimelineObj :: GetPropertySetter, méthode</span><span class="sxs-lookup"><span data-stu-id="2e2b0-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="2e2b0-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-105">\[Deprecated.</span></span> <span data-ttu-id="2e2b0-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e2b0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e2b0-107">La `GetPropertySetter` méthode récupère l’accesseur Set de la propriété de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="2e2b0-108">Lorsque l’objet est rendu, les informations de propriété contenues dans l’accesseur Set de propriété sont appliquées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2b0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e2b0-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="2e2b0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e2b0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e2b0-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2e2b0-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2e2b0-112">Reçoit un pointeur vers l’interface [**IPropertySetter**](ipropertysetter.md) de l’accesseur Set de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="2e2b0-113">Si l’objet n’a pas de méthode setter de propriété, la valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e2b0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e2b0-114">Return value</span></span>

<span data-ttu-id="2e2b0-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e2b0-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e2b0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2b0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2e2b0-117">Remarks</span></span>

<span data-ttu-id="2e2b0-118">Si la valeur retournée dans *pval* n’est pas **null**, l’interface **IPropertySetter** a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="2e2b0-119">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="2e2b0-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e2b0-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e2b0-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e2b0-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2e2b0-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e2b0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e2b0-123">Requirements</span></span>



| <span data-ttu-id="2e2b0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e2b0-124">Requirement</span></span> | <span data-ttu-id="2e2b0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e2b0-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2b0-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e2b0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2e2b0-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2b0-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e2b0-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e2b0-128">Library</span></span><br/> | <dl> <span data-ttu-id="2e2b0-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e2b0-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2b0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2b0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2b0-131">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="2e2b0-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="2e2b0-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="2e2b0-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




