---
description: La \_ méthode put Invert spécifie si l’opération de clé est inversée. Cette propriété s’applique à tous les types de clés, à l’exception de DXTKEY \_ alpha.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: IDxtKey ::p ut_Invert, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525211"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="5e990-104">IDxtKey ::p ut \_ inversé, méthode</span><span class="sxs-lookup"><span data-stu-id="5e990-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="5e990-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5e990-105">\[Deprecated.</span></span> <span data-ttu-id="5e990-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e990-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5e990-107">La `put_Invert` méthode spécifie si l’opération de clé est inversée.</span><span class="sxs-lookup"><span data-stu-id="5e990-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="5e990-108">Cette propriété s’applique à tous les types de clés, à l’exception de DXTKEY \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="5e990-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e990-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e990-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="5e990-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e990-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e990-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e990-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e990-112">Spécifie une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="5e990-112">Specifies a Boolean value.</span></span> <span data-ttu-id="5e990-113">Si la **valeur est true**, les pixels de l’image superposée sont inversés par rapport à l’opération par défaut.</span><span class="sxs-lookup"><span data-stu-id="5e990-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="5e990-114">Si la **valeur est false**, les pixels de l’image superposée sont rendus transparents par défaut.</span><span class="sxs-lookup"><span data-stu-id="5e990-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e990-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e990-115">Return value</span></span>

<span data-ttu-id="5e990-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5e990-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e990-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e990-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e990-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5e990-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5e990-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5e990-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5e990-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e990-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5e990-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5e990-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e990-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e990-122">Requirements</span></span>



| <span data-ttu-id="5e990-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e990-123">Requirement</span></span> | <span data-ttu-id="5e990-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e990-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e990-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e990-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5e990-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e990-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5e990-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e990-127">Library</span></span><br/> | <dl> <span data-ttu-id="5e990-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e990-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e990-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e990-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e990-130">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="5e990-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="5e990-131">**IDxtKey ::p \_ type ut**</span><span class="sxs-lookup"><span data-stu-id="5e990-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




