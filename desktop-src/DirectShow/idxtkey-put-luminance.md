---
description: La \_ méthode put luminance spécifie la valeur de luminance sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ luminance.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: IDxtKey ::p ut_Luminance, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528815"
---
# <a name="idxtkeyput_luminance-method"></a><span data-ttu-id="fb156-104">IDxtKey : méthode de \_ Luminance :p ut</span><span class="sxs-lookup"><span data-stu-id="fb156-104">IDxtKey::put\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="fb156-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fb156-105">\[Deprecated.</span></span> <span data-ttu-id="fb156-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb156-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb156-107">La `put_Luminance` méthode spécifie la valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="fb156-107">The `put_Luminance` method specifies the luminance value on which to key.</span></span> <span data-ttu-id="fb156-108">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ luminance.</span><span class="sxs-lookup"><span data-stu-id="fb156-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb156-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb156-109">Syntax</span></span>


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fb156-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb156-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb156-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb156-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb156-112">Valeur de luminance sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="fb156-112">The luminance value on which to key.</span></span> <span data-ttu-id="fb156-113">La plage valide est comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="fb156-113">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb156-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb156-114">Return value</span></span>

<span data-ttu-id="fb156-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fb156-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb156-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb156-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb156-117">Notes</span><span class="sxs-lookup"><span data-stu-id="fb156-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb156-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="fb156-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb156-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb156-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fb156-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fb156-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb156-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb156-121">Requirements</span></span>



| <span data-ttu-id="fb156-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb156-122">Requirement</span></span> | <span data-ttu-id="fb156-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb156-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb156-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb156-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb156-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb156-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb156-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb156-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb156-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb156-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb156-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb156-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb156-129">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="fb156-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="fb156-130">**IDxtKey ::p \_ type ut**</span><span class="sxs-lookup"><span data-stu-id="fb156-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




