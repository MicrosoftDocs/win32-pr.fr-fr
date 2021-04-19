---
description: Obtient les informations de catégorie d’un élément.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2 :: GetItemCategory, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516885"
---
# <a name="iwiaitem2getitemcategory-method"></a><span data-ttu-id="8241b-103">IWiaItem2 :: GetItemCategory, méthode</span><span class="sxs-lookup"><span data-stu-id="8241b-103">IWiaItem2::GetItemCategory method</span></span>

<span data-ttu-id="8241b-104">Obtient les informations de catégorie d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8241b-104">Gets an item's category information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8241b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8241b-105">Syntax</span></span>


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a><span data-ttu-id="8241b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8241b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8241b-107">*pItemCategoryGUID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8241b-107">*pItemCategoryGUID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8241b-108">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8241b-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="8241b-109">Reçoit un pointeur vers le GUID qui identifie la catégorie de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8241b-109">Receives a pointer to the GUID that identifies the category of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8241b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8241b-110">Return value</span></span>

<span data-ttu-id="8241b-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8241b-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8241b-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8241b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8241b-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8241b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8241b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8241b-114">Remarks</span></span>

<span data-ttu-id="8241b-115">Chaque objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence hiérarchique d’objets associés à un périphérique matériel WIA (Windows Image Acquisition) 2,0 a une catégorie spécifique.</span><span class="sxs-lookup"><span data-stu-id="8241b-115">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific category.</span></span> <span data-ttu-id="8241b-116">Cette méthode permet aux applications d’identifier la catégorie d’un élément dans une arborescence hiérarchique d’objets Item dans un appareil.</span><span class="sxs-lookup"><span data-stu-id="8241b-116">This method enables applications to identify the category of any item in a hierarchical tree of item objects in a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="8241b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8241b-117">Requirements</span></span>



| <span data-ttu-id="8241b-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8241b-118">Requirement</span></span> | <span data-ttu-id="8241b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8241b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8241b-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8241b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8241b-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8241b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8241b-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8241b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8241b-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8241b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8241b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8241b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8241b-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8241b-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8241b-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="8241b-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8241b-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8241b-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 




