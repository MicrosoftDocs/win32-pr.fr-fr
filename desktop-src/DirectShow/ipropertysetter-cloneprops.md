---
description: La méthode CloneProps clone un ensemble de propriétés à partir de cet accesseur Set de propriété et les ajoute à un nouvel accesseur Set de propriété.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'IPropertySetter :: CloneProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532769"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="223d7-103">IPropertySetter :: CloneProps, méthode</span><span class="sxs-lookup"><span data-stu-id="223d7-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="223d7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="223d7-104">\[Deprecated.</span></span> <span data-ttu-id="223d7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="223d7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="223d7-106">La `CloneProps` méthode Clone un jeu de propriétés à partir de cet accesseur Set de propriété et les ajoute à un nouvel accesseur Set de propriété.</span><span class="sxs-lookup"><span data-stu-id="223d7-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="223d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="223d7-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="223d7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="223d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="223d7-109">*ppSetter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="223d7-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="223d7-110">Reçoit un pointeur vers l’interface **IPropertySetter** du nouvel accesseur Set de propriété.</span><span class="sxs-lookup"><span data-stu-id="223d7-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="223d7-111">*rtStart* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="223d7-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d7-112">Heure de début de la plage de valeurs à cloner, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="223d7-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="223d7-113">*rtStop* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="223d7-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="223d7-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="223d7-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="223d7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="223d7-115">Return value</span></span>

<span data-ttu-id="223d7-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="223d7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="223d7-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="223d7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="223d7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="223d7-118">Remarks</span></span>

<span data-ttu-id="223d7-119">Seules les valeurs qui tombent après l’heure de début spécifiée sont clonées.</span><span class="sxs-lookup"><span data-stu-id="223d7-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="223d7-120">Les heures sur les valeurs clonées sont ensuite ajustées par rapport à l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="223d7-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="223d7-121">Par exemple, si *rtStart* est 20 millions (2 secondes), une valeur à l’heure 30 millions (3 secondes) est clonée avec l’heure 10 millions (1 seconde).</span><span class="sxs-lookup"><span data-stu-id="223d7-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="223d7-122">Enfin, chaque propriété clonée reçoit une valeur initiale égale à la valeur de la propriété d’origine à l’heure de début (correctement interpolée si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="223d7-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="223d7-123">En effet, les données de propriété sont fractionnées à l’heure de début spécifiée.</span><span class="sxs-lookup"><span data-stu-id="223d7-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="223d7-124">Si la méthode est réussie, l’interface [**IPropertySetter**](ipropertysetter.md) qu’elle retourne a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="223d7-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="223d7-125">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="223d7-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="223d7-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="223d7-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="223d7-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="223d7-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="223d7-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="223d7-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="223d7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="223d7-129">Requirements</span></span>



| <span data-ttu-id="223d7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="223d7-130">Requirement</span></span> | <span data-ttu-id="223d7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="223d7-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="223d7-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="223d7-132">Header</span></span><br/>  | <dl> <span data-ttu-id="223d7-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="223d7-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="223d7-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="223d7-134">Library</span></span><br/> | <dl> <span data-ttu-id="223d7-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="223d7-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="223d7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="223d7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223d7-137">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="223d7-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="223d7-138">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="223d7-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




