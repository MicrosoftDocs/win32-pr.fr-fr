---
description: La méthode ClearProps efface toutes les données de propriété de l’accesseur Set de propriété. L’application peut définir de nouvelles données de propriété après l’appel de cette fonction.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'IPropertySetter :: ClearProps, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528424"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="02710-104">IPropertySetter :: ClearProps, méthode</span><span class="sxs-lookup"><span data-stu-id="02710-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="02710-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="02710-105">\[Deprecated.</span></span> <span data-ttu-id="02710-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02710-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="02710-107">La `ClearProps` méthode efface toutes les données de propriété de l’accesseur Set de propriété.</span><span class="sxs-lookup"><span data-stu-id="02710-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="02710-108">L’application peut définir de nouvelles données de propriété après l’appel de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="02710-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="02710-109">L’effacement des données de propriété ne restaure pas les propriétés de l’objet à leurs valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="02710-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="02710-110">Il empêche simplement DirectShow d’appliquer d’autres modifications.</span><span class="sxs-lookup"><span data-stu-id="02710-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="02710-111">Les valeurs de propriété sont appliquées au moment de l’exécution lorsque le projet est restitué.</span><span class="sxs-lookup"><span data-stu-id="02710-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="02710-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02710-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="02710-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02710-113">Parameters</span></span>

<span data-ttu-id="02710-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="02710-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02710-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02710-115">Return value</span></span>

<span data-ttu-id="02710-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="02710-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02710-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02710-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="02710-118">Notes</span><span class="sxs-lookup"><span data-stu-id="02710-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02710-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="02710-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="02710-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="02710-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="02710-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="02710-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02710-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02710-122">Requirements</span></span>



| <span data-ttu-id="02710-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02710-123">Requirement</span></span> | <span data-ttu-id="02710-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="02710-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02710-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="02710-125">Header</span></span><br/>  | <dl> <span data-ttu-id="02710-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="02710-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="02710-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02710-127">Library</span></span><br/> | <dl> <span data-ttu-id="02710-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02710-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02710-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02710-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02710-130">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="02710-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="02710-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="02710-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




