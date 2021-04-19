---
description: La méthode AddProp ajoute une propriété à la méthode setter de propriété, avec un tableau de paires heure-valeur qui définissent la valeur de la propriété sur une plage de temps.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'IPropertySetter :: AddProp, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542241"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="99471-103">IPropertySetter :: AddProp, méthode</span><span class="sxs-lookup"><span data-stu-id="99471-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="99471-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="99471-104">\[Deprecated.</span></span> <span data-ttu-id="99471-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99471-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="99471-106">La `AddProp` méthode ajoute une propriété à la méthode setter de propriété, avec un tableau de paires heure-valeur qui définissent la valeur de la propriété sur une plage de temps.</span><span class="sxs-lookup"><span data-stu-id="99471-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="99471-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99471-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="99471-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99471-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99471-109">*Param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99471-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99471-110">[**Dexterity \_ Structure PARAM**](dexter-param.md) qui spécifie la propriété.</span><span class="sxs-lookup"><span data-stu-id="99471-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="99471-111">Le membre **nvaleurs** de la structure doit être égal à la taille du tableau donné dans le paramètre *paValue* .</span><span class="sxs-lookup"><span data-stu-id="99471-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="99471-112">*paValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99471-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99471-113">Pointeur vers un tableau de structures de [**\_ valeur Dexter**](dexter-value.md) qui contiennent des paires heure-valeur.</span><span class="sxs-lookup"><span data-stu-id="99471-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="99471-114">Le tableau doit être dans l’ordre chronologique croissant.</span><span class="sxs-lookup"><span data-stu-id="99471-114">The array must be in ascending time order.</span></span> <span data-ttu-id="99471-115">Les heures sont relatives à l’heure de début de l’effet ou de la transition.</span><span class="sxs-lookup"><span data-stu-id="99471-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99471-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99471-116">Return value</span></span>

<span data-ttu-id="99471-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="99471-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99471-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="99471-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="99471-119">Notes</span><span class="sxs-lookup"><span data-stu-id="99471-119">Remarks</span></span>

<span data-ttu-id="99471-120">La première structure de [**\_ valeur Dexterity**](dexter-value.md) doit spécifier un temps de référence de zéro et un indicateur d’interpolation (**dwInterp**) de **DEXTERF \_ Jump**, ou la méthode retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="99471-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="99471-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="99471-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="99471-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="99471-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="99471-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="99471-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99471-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99471-124">Requirements</span></span>



| <span data-ttu-id="99471-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99471-125">Requirement</span></span> | <span data-ttu-id="99471-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="99471-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99471-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="99471-127">Header</span></span><br/>  | <dl> <span data-ttu-id="99471-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="99471-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="99471-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="99471-129">Library</span></span><br/> | <dl> <span data-ttu-id="99471-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99471-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99471-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99471-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99471-132">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="99471-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="99471-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="99471-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




