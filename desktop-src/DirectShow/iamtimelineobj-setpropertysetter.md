---
description: La méthode SetPropertySetter définit l’accesseur Set de la propriété de l’objet. Lorsque l’objet est rendu, les informations de propriété contenues dans l’accesseur Set de propriété sont appliquées à l’objet. Appelez cette méthode sur les objets de transition et d’effet.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'IAMTimelineObj :: SetPropertySetter, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539988"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="b9d18-105">IAMTimelineObj :: SetPropertySetter, méthode</span><span class="sxs-lookup"><span data-stu-id="b9d18-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="b9d18-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b9d18-106">\[Deprecated.</span></span> <span data-ttu-id="b9d18-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b9d18-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b9d18-108">La `SetPropertySetter` méthode définit l’accesseur Set de la propriété de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b9d18-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="b9d18-109">Lorsque l’objet est rendu, les informations de propriété contenues dans l’accesseur Set de propriété sont appliquées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="b9d18-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="b9d18-110">Appelez cette méthode sur les objets de transition et d’effet.</span><span class="sxs-lookup"><span data-stu-id="b9d18-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d18-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9d18-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="b9d18-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9d18-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9d18-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="b9d18-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="b9d18-114">Pointeur vers l’interface [**IPropertySetter**](ipropertysetter.md) de l’accesseur Set de la propriété.</span><span class="sxs-lookup"><span data-stu-id="b9d18-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9d18-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9d18-115">Return value</span></span>

<span data-ttu-id="b9d18-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9d18-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9d18-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9d18-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d18-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b9d18-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b9d18-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b9d18-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9d18-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9d18-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b9d18-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b9d18-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b9d18-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9d18-122">Requirements</span></span>



| <span data-ttu-id="b9d18-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9d18-123">Requirement</span></span> | <span data-ttu-id="b9d18-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9d18-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9d18-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9d18-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b9d18-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9d18-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b9d18-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9d18-127">Library</span></span><br/> | <dl> <span data-ttu-id="b9d18-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9d18-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9d18-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9d18-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9d18-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b9d18-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b9d18-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b9d18-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




