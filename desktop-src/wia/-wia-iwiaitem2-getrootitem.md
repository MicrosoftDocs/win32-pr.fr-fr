---
description: Obtient l’élément racine d’une arborescence d’objets d’élément utilisés pour représenter un périphérique matériel WIA (Windows Image Acquisition) 2,0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: 'IWiaItem2 :: GetRootItem, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751780"
---
# <a name="iwiaitem2getrootitem-method"></a><span data-ttu-id="e6c78-103">IWiaItem2 :: GetRootItem, méthode</span><span class="sxs-lookup"><span data-stu-id="e6c78-103">IWiaItem2::GetRootItem method</span></span>

<span data-ttu-id="e6c78-104">Obtient l’élément racine d’une arborescence d’objets d’élément utilisés pour représenter un périphérique matériel WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="e6c78-104">Gets the root item of a tree of item objects used to represent a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6c78-105">Syntax</span></span>


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="e6c78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6c78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c78-107">*ppIWiaItem2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6c78-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6c78-108">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e6c78-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="e6c78-109">Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément racine.</span><span class="sxs-lookup"><span data-stu-id="e6c78-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c78-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6c78-110">Return value</span></span>

<span data-ttu-id="e6c78-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6c78-111">Type: **HRESULT**</span></span>

<span data-ttu-id="e6c78-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6c78-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6c78-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6c78-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6c78-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e6c78-114">Remarks</span></span>

<span data-ttu-id="e6c78-115">À partir de n’importe quel objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence d’objets d’un périphérique matériel WIA 2,0, l’application récupère un pointeur vers l’élément racine en appelant cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e6c78-115">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the root item by calling this function.</span></span>

<span data-ttu-id="e6c78-116">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="e6c78-116">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c78-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6c78-117">Requirements</span></span>



| <span data-ttu-id="e6c78-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6c78-118">Requirement</span></span> | <span data-ttu-id="e6c78-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6c78-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c78-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6c78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c78-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6c78-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e6c78-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6c78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c78-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6c78-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e6c78-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6c78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c78-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c78-125"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6c78-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="e6c78-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6c78-127"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6c78-127"><dt>Wia.idl</dt></span></span> </dl> |



 

 
