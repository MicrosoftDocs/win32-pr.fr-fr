---
description: La \_ méthode obtenir KeyType récupère le type de clé.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'IDxtKey :: get_KeyType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533023"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="17ca5-103">IDxtKey :: obtient la \_ méthode KeyType</span><span class="sxs-lookup"><span data-stu-id="17ca5-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="17ca5-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="17ca5-104">\[Deprecated.</span></span> <span data-ttu-id="17ca5-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17ca5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17ca5-106">La `get_KeyType` méthode récupère le type de clé.</span><span class="sxs-lookup"><span data-stu-id="17ca5-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ca5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17ca5-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="17ca5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17ca5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ca5-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="17ca5-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca5-110">Reçoit l’une des valeurs d’énumération suivantes.</span><span class="sxs-lookup"><span data-stu-id="17ca5-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="17ca5-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="17ca5-111">Value</span></span>             | <span data-ttu-id="17ca5-112">Description</span><span class="sxs-lookup"><span data-stu-id="17ca5-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="17ca5-113">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="17ca5-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="17ca5-114">Clé Chroma.</span><span class="sxs-lookup"><span data-stu-id="17ca5-114">Chroma key.</span></span> <span data-ttu-id="17ca5-115">(Clé sur la valeur RVB.)</span><span class="sxs-lookup"><span data-stu-id="17ca5-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="17ca5-116">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="17ca5-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="17ca5-117">Clé Nonred.</span><span class="sxs-lookup"><span data-stu-id="17ca5-117">Nonred key.</span></span> <span data-ttu-id="17ca5-118">(Rend les zones bleues et vertes transparentes.)</span><span class="sxs-lookup"><span data-stu-id="17ca5-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="17ca5-119">\_luminance DXTKEY</span><span class="sxs-lookup"><span data-stu-id="17ca5-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="17ca5-120">Clé de luminance.</span><span class="sxs-lookup"><span data-stu-id="17ca5-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="17ca5-121">DXTKEY \_ alpha</span><span class="sxs-lookup"><span data-stu-id="17ca5-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="17ca5-122">Clé par valeur alpha.</span><span class="sxs-lookup"><span data-stu-id="17ca5-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="17ca5-123">DXTKEY \_ teinte</span><span class="sxs-lookup"><span data-stu-id="17ca5-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="17ca5-124">Clé par teinte.</span><span class="sxs-lookup"><span data-stu-id="17ca5-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ca5-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17ca5-125">Return value</span></span>

<span data-ttu-id="17ca5-126">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17ca5-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17ca5-127">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17ca5-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ca5-128">Notes</span><span class="sxs-lookup"><span data-stu-id="17ca5-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="17ca5-129">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="17ca5-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17ca5-130">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="17ca5-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17ca5-131">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="17ca5-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17ca5-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17ca5-132">Requirements</span></span>



| <span data-ttu-id="17ca5-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17ca5-133">Requirement</span></span> | <span data-ttu-id="17ca5-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="17ca5-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17ca5-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="17ca5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="17ca5-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="17ca5-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17ca5-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17ca5-137">Library</span></span><br/> | <dl> <span data-ttu-id="17ca5-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17ca5-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ca5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17ca5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ca5-140">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="17ca5-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




