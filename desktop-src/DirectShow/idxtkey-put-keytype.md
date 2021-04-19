---
description: La \_ méthode put KeyType spécifie le type de clé.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: IDxtKey ::p ut_KeyType, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545431"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="593f4-103">IDxtKey ::p \_ méthode de frappe de type ut</span><span class="sxs-lookup"><span data-stu-id="593f4-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="593f4-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="593f4-104">\[Deprecated.</span></span> <span data-ttu-id="593f4-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="593f4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="593f4-106">La `put_KeyType` méthode spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="593f4-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="593f4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="593f4-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="593f4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="593f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="593f4-109">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="593f4-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="593f4-110">Spécifie le type de clé.</span><span class="sxs-lookup"><span data-stu-id="593f4-110">Specifies the key type.</span></span> <span data-ttu-id="593f4-111">Ce paramètre doit être l’une des valeurs d’énumération suivantes.</span><span class="sxs-lookup"><span data-stu-id="593f4-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="593f4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="593f4-112">Value</span></span>             | <span data-ttu-id="593f4-113">Description</span><span class="sxs-lookup"><span data-stu-id="593f4-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="593f4-114">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="593f4-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="593f4-115">Clé Chroma.</span><span class="sxs-lookup"><span data-stu-id="593f4-115">Chroma key.</span></span> <span data-ttu-id="593f4-116">(Clé sur la valeur RVB.)</span><span class="sxs-lookup"><span data-stu-id="593f4-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="593f4-117">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="593f4-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="593f4-118">Clé Nonred.</span><span class="sxs-lookup"><span data-stu-id="593f4-118">Nonred key.</span></span> <span data-ttu-id="593f4-119">(Rend les zones bleues et vertes transparentes.)</span><span class="sxs-lookup"><span data-stu-id="593f4-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="593f4-120">\_luminance DXTKEY</span><span class="sxs-lookup"><span data-stu-id="593f4-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="593f4-121">Clé de luminance.</span><span class="sxs-lookup"><span data-stu-id="593f4-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="593f4-122">DXTKEY \_ alpha</span><span class="sxs-lookup"><span data-stu-id="593f4-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="593f4-123">Clé par valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="593f4-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="593f4-124">DXTKEY \_ teinte</span><span class="sxs-lookup"><span data-stu-id="593f4-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="593f4-125">Clé par teinte.</span><span class="sxs-lookup"><span data-stu-id="593f4-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="593f4-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="593f4-126">Return value</span></span>

<span data-ttu-id="593f4-127">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="593f4-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="593f4-128">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="593f4-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="593f4-129">Notes</span><span class="sxs-lookup"><span data-stu-id="593f4-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="593f4-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="593f4-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="593f4-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="593f4-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="593f4-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="593f4-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="593f4-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="593f4-133">Requirements</span></span>



| <span data-ttu-id="593f4-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="593f4-134">Requirement</span></span> | <span data-ttu-id="593f4-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="593f4-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="593f4-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="593f4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="593f4-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="593f4-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="593f4-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="593f4-138">Library</span></span><br/> | <dl> <span data-ttu-id="593f4-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="593f4-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="593f4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="593f4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="593f4-141">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="593f4-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




