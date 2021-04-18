---
description: La \_ méthode put Hue spécifie la valeur de teinte sur laquelle la clé doit être ajoutée. Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ teinte.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: IDxtKey ::p ut_Hue, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540410"
---
# <a name="idxtkeyput_hue-method"></a><span data-ttu-id="0ea3e-104">IDxtKey ::p \_ méthode de teinte ut</span><span class="sxs-lookup"><span data-stu-id="0ea3e-104">IDxtKey::put\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="0ea3e-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-105">\[Deprecated.</span></span> <span data-ttu-id="0ea3e-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ea3e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0ea3e-107">La `put_Hue` méthode spécifie la valeur de teinte sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-107">The `put_Hue` method specifies the hue value on which to key.</span></span> <span data-ttu-id="0ea3e-108">Cette propriété s’applique uniquement lorsque le type de clé est DXTKEY \_ teinte.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea3e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea3e-109">Syntax</span></span>


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="0ea3e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ea3e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea3e-111">*newVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ea3e-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea3e-112">Valeur de teinte sur laquelle la clé doit être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-112">The hue value on which to key.</span></span> <span data-ttu-id="0ea3e-113">La plage valide est comprise entre 0 et 360.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-113">The valid range is from 0 to 360.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea3e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ea3e-114">Return value</span></span>

<span data-ttu-id="0ea3e-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ea3e-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ea3e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea3e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0ea3e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0ea3e-118">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0ea3e-119">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0ea3e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0ea3e-120">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0ea3e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0ea3e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ea3e-121">Requirements</span></span>



| <span data-ttu-id="0ea3e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ea3e-122">Requirement</span></span> | <span data-ttu-id="0ea3e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ea3e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea3e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ea3e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0ea3e-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea3e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0ea3e-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ea3e-126">Library</span></span><br/> | <dl> <span data-ttu-id="0ea3e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ea3e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea3e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea3e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea3e-129">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="0ea3e-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="0ea3e-130">**IDxtKey ::p \_ type ut**</span><span class="sxs-lookup"><span data-stu-id="0ea3e-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




