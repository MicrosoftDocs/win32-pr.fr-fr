---
description: La \_ méthode put RGB spécifie la couleur RVB sur laquelle la touche est enfoncée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: IDxtKey ::p ut_RGB, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540538"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="bb311-104">IDxtKey : méthode :p ut \_ RGB</span><span class="sxs-lookup"><span data-stu-id="bb311-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="bb311-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bb311-105">\[Deprecated.</span></span> <span data-ttu-id="bb311-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bb311-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bb311-107">La `put_RGB` méthode spécifie la couleur RVB sur laquelle la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="bb311-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="bb311-108">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="bb311-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb311-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb311-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="bb311-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb311-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb311-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb311-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb311-112">Spécifie la couleur sous la forme d’un nombre hexadécimal au format 0xRRGGBB, où RR est la valeur rouge, GG est la valeur verte et BB est la valeur bleue.</span><span class="sxs-lookup"><span data-stu-id="bb311-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb311-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb311-113">Return value</span></span>

<span data-ttu-id="bb311-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb311-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb311-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb311-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb311-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bb311-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bb311-117">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="bb311-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bb311-118">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb311-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bb311-119">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bb311-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bb311-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb311-120">Requirements</span></span>



| <span data-ttu-id="bb311-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb311-121">Requirement</span></span> | <span data-ttu-id="bb311-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb311-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb311-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb311-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bb311-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb311-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bb311-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb311-125">Library</span></span><br/> | <dl> <span data-ttu-id="bb311-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb311-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb311-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb311-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb311-128">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="bb311-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="bb311-129">**IDxtKey ::p \_ type ut**</span><span class="sxs-lookup"><span data-stu-id="bb311-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




