---
description: 'La méthode FreeProps libère les ressources allouées par la méthode IPropertySetter :: GetProps. Appelez cette méthode après avoir appelé GetProps, en lui transmettant les structures retournées par GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'IPropertySetter :: FreeProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530947"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="9de14-104">IPropertySetter :: FreeProps, méthode</span><span class="sxs-lookup"><span data-stu-id="9de14-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="9de14-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9de14-105">\[Deprecated.</span></span> <span data-ttu-id="9de14-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9de14-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9de14-107">La `FreeProps` méthode libère les ressources allouées par la méthode [**IPropertySetter :: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="9de14-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="9de14-108">Appelez cette méthode après avoir appelé **GetProps**, en lui transmettant les structures retournées par **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="9de14-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de14-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9de14-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="9de14-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9de14-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de14-111">*cParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9de14-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de14-112">Nombre d’éléments dans le tableau *paParam* .</span><span class="sxs-lookup"><span data-stu-id="9de14-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="9de14-113">*paParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9de14-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de14-114">Pointeur vers un tableau de structures de [**\_ paramètres Dexter**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="9de14-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="9de14-115">*paValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9de14-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de14-116">Pointeur vers un tableau de structures de [**\_ valeur Dexterity**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="9de14-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de14-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9de14-117">Return value</span></span>

<span data-ttu-id="9de14-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9de14-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de14-119">Notes</span><span class="sxs-lookup"><span data-stu-id="9de14-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9de14-120">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9de14-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9de14-121">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9de14-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9de14-122">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9de14-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9de14-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9de14-123">Requirements</span></span>



| <span data-ttu-id="9de14-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9de14-124">Requirement</span></span> | <span data-ttu-id="9de14-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9de14-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9de14-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9de14-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9de14-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de14-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9de14-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9de14-128">Library</span></span><br/> | <dl> <span data-ttu-id="9de14-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9de14-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de14-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9de14-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de14-131">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="9de14-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="9de14-132">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="9de14-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




