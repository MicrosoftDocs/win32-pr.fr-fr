---
description: La méthode obtenir des \_ couleurs RVB permet de récupérer la couleur RVB sur laquelle la touche est enfoncée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'IDxtKey :: get_RGB, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525212"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="81f60-104">IDxtKey :: obtient la \_ méthode RGB</span><span class="sxs-lookup"><span data-stu-id="81f60-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="81f60-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="81f60-105">\[Deprecated.</span></span> <span data-ttu-id="81f60-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81f60-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81f60-107">La `get_RGB` méthode récupère la couleur RVB sur laquelle la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="81f60-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="81f60-108">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="81f60-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f60-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81f60-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="81f60-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81f60-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f60-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="81f60-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="81f60-112">Reçoit la couleur.</span><span class="sxs-lookup"><span data-stu-id="81f60-112">Receives the color.</span></span> <span data-ttu-id="81f60-113">La valeur retournée est un nombre hexadécimal au format 0xRRGGBB, où RR est la valeur rouge, GG est la valeur verte et BB est la valeur bleue.</span><span class="sxs-lookup"><span data-stu-id="81f60-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f60-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81f60-114">Return value</span></span>

<span data-ttu-id="81f60-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="81f60-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81f60-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81f60-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f60-117">Notes</span><span class="sxs-lookup"><span data-stu-id="81f60-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81f60-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="81f60-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81f60-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="81f60-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81f60-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="81f60-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81f60-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81f60-121">Requirements</span></span>



| <span data-ttu-id="81f60-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81f60-122">Requirement</span></span> | <span data-ttu-id="81f60-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="81f60-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81f60-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="81f60-124">Header</span></span><br/>  | <dl> <span data-ttu-id="81f60-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f60-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81f60-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81f60-126">Library</span></span><br/> | <dl> <span data-ttu-id="81f60-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81f60-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f60-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81f60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f60-129">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="81f60-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="81f60-130">**IDxtKey :: obtient \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="81f60-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




