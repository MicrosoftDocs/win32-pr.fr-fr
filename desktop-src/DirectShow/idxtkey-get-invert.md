---
description: La \_ méthode obtenir une inversion récupère une valeur booléenne indiquant si l’opération de clé est inversée. Cette propriété s’applique à tous les types de clés, à l’exception de DXTKEY \_ alpha.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'IDxtKey :: get_Invert, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540243"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="5d2a2-104">IDxtKey :: obtient la \_ méthode inversée</span><span class="sxs-lookup"><span data-stu-id="5d2a2-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="5d2a2-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-105">\[Deprecated.</span></span> <span data-ttu-id="5d2a2-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d2a2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d2a2-107">La `get_Invert` méthode récupère une valeur booléenne indiquant si l’opération de clé est inversée.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="5d2a2-108">Cette propriété s’applique à tous les types de clés, à l’exception de DXTKEY \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2a2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d2a2-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5d2a2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d2a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2a2-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5d2a2-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2a2-112">Reçoit l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-112">Receives one of the following values.</span></span>



| <span data-ttu-id="5d2a2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d2a2-113">Value</span></span>     | <span data-ttu-id="5d2a2-114">Description</span><span class="sxs-lookup"><span data-stu-id="5d2a2-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d2a2-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5d2a2-115">**TRUE**</span></span>  | <span data-ttu-id="5d2a2-116">Les pixels de l’image superposée sont inversés par rapport à l’opération par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="5d2a2-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5d2a2-117">**FALSE**</span></span> | <span data-ttu-id="5d2a2-118">Les pixels de l’image superposée sont rendus transparents par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2a2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d2a2-119">Return value</span></span>

<span data-ttu-id="5d2a2-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d2a2-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d2a2-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d2a2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5d2a2-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d2a2-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d2a2-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5d2a2-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5d2a2-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5d2a2-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d2a2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d2a2-126">Requirements</span></span>



| <span data-ttu-id="5d2a2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d2a2-127">Requirement</span></span> | <span data-ttu-id="5d2a2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d2a2-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2a2-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d2a2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5d2a2-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2a2-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d2a2-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d2a2-131">Library</span></span><br/> | <dl> <span data-ttu-id="5d2a2-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d2a2-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2a2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2a2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2a2-134">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="5d2a2-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="5d2a2-135">**IDxtKey :: obtient \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="5d2a2-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




