---
description: Obtient les informations de type d’un élément.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2 :: GetItemType, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751781"
---
# <a name="iwiaitem2getitemtype-method"></a><span data-ttu-id="ff89b-103">IWiaItem2 :: GetItemType, méthode</span><span class="sxs-lookup"><span data-stu-id="ff89b-103">IWiaItem2::GetItemType method</span></span>

<span data-ttu-id="ff89b-104">Obtient les informations de type d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ff89b-104">Gets an item's type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff89b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff89b-105">Syntax</span></span>


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a><span data-ttu-id="ff89b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff89b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff89b-107">*pItemType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ff89b-107">*pItemType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff89b-108">Type : \**long \** _</span><span class="sxs-lookup"><span data-stu-id="ff89b-108">Type: \**LONG\** _</span></span>

<span data-ttu-id="ff89b-109">Reçoit un pointeur vers un _ *long*\* qui contient une combinaison d’indicateurs de type.</span><span class="sxs-lookup"><span data-stu-id="ff89b-109">Receives a pointer to a _ *LONG*\* that contains a combination of type flags.</span></span> <span data-ttu-id="ff89b-110">Consultez [**indicateurs de type d’élément WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ff89b-110">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff89b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff89b-111">Return value</span></span>

<span data-ttu-id="ff89b-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ff89b-112">Type: **HRESULT**</span></span>

<span data-ttu-id="ff89b-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff89b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff89b-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff89b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff89b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ff89b-115">Remarks</span></span>

<span data-ttu-id="ff89b-116">Chaque objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence hiérarchique d’objets associés à un périphérique matériel WIA (Windows Image Acquisition) 2,0 a un type de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="ff89b-116">Every [**IWiaItem2**](-wia-iwiaitem2.md) object in the hierarchical tree of objects associated with a Windows Image Acquisition (WIA) 2.0 hardware device has a specific data type.</span></span> <span data-ttu-id="ff89b-117">Les objets Item représentent des dossiers et des fichiers.</span><span class="sxs-lookup"><span data-stu-id="ff89b-117">Item objects represent folders and files.</span></span> <span data-ttu-id="ff89b-118">Les dossiers contiennent des objets de fichier.</span><span class="sxs-lookup"><span data-stu-id="ff89b-118">Folders contain file objects.</span></span> <span data-ttu-id="ff89b-119">Les objets fichier contiennent des données acquises par l’appareil, telles que des images et des sons.</span><span class="sxs-lookup"><span data-stu-id="ff89b-119">File objects contain data acquired by the device such as images and sounds.</span></span> <span data-ttu-id="ff89b-120">Cette méthode permet aux applications d’identifier le type d’un élément dans une arborescence hiérarchique d’objets Item dans un appareil.</span><span class="sxs-lookup"><span data-stu-id="ff89b-120">This method enables applications to identify the type of any item in a hierarchical tree of item objects in a device.</span></span>

<span data-ttu-id="ff89b-121">Un élément peut avoir plusieurs types.</span><span class="sxs-lookup"><span data-stu-id="ff89b-121">An item may have more than one type.</span></span> <span data-ttu-id="ff89b-122">Par exemple, un élément qui représente un fichier audio aura les attributs de type [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span><span class="sxs-lookup"><span data-stu-id="ff89b-122">For example, an item that represents an audio file will have the type attributes [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff89b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff89b-123">Requirements</span></span>



| <span data-ttu-id="ff89b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff89b-124">Requirement</span></span> | <span data-ttu-id="ff89b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff89b-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff89b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff89b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff89b-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff89b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ff89b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff89b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff89b-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff89b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ff89b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff89b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff89b-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff89b-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff89b-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="ff89b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff89b-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff89b-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 




