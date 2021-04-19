---
description: La méthode SetProps définit les propriétés de l’objet cible à l’état approprié pour l’heure spécifiée.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'IPropertySetter :: SetProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525510"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="2d58c-103">IPropertySetter :: SetProps, méthode</span><span class="sxs-lookup"><span data-stu-id="2d58c-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="2d58c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2d58c-104">\[Deprecated.</span></span> <span data-ttu-id="2d58c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d58c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d58c-106">La `SetProps` méthode définit les propriétés de l’objet cible à l’état approprié pour l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2d58c-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d58c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d58c-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="2d58c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d58c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d58c-109">*pTarget* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d58c-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d58c-110">Pointeur vers l’objet cible pour lequel définir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="2d58c-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="2d58c-111">*rtNow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d58c-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d58c-112">Heure à laquelle définir les propriétés, en unités de 100 nanosecondes, ou-1 pour définir des propriétés statiques (celles qui ne varient pas au fil du temps).</span><span class="sxs-lookup"><span data-stu-id="2d58c-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d58c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d58c-113">Return value</span></span>

<span data-ttu-id="2d58c-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2d58c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d58c-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d58c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d58c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2d58c-116">Remarks</span></span>

<span data-ttu-id="2d58c-117">Cette méthode est appelée par DES pour définir les propriétés sur une transition ou un effet.</span><span class="sxs-lookup"><span data-stu-id="2d58c-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="2d58c-118">Une application n’appelle normalement pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2d58c-118">An application will not normally call this method.</span></span>

<span data-ttu-id="2d58c-119">L’objet spécifié par *pTarget* doit implémenter l’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="2d58c-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="2d58c-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="2d58c-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d58c-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2d58c-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d58c-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2d58c-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d58c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d58c-123">Requirements</span></span>



| <span data-ttu-id="2d58c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d58c-124">Requirement</span></span> | <span data-ttu-id="2d58c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d58c-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d58c-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d58c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2d58c-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d58c-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d58c-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d58c-128">Library</span></span><br/> | <dl> <span data-ttu-id="2d58c-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d58c-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d58c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d58c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d58c-131">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="2d58c-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="2d58c-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="2d58c-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




