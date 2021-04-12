---
description: Obtient l’élément parent dans l’arborescence qui représente un périphérique matériel WIA (Windows Image Acquisition) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2 :: GetParentItem, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318442"
---
# <a name="iwiaitem2getparentitem-method"></a><span data-ttu-id="fae88-103">IWiaItem2 :: GetParentItem, méthode</span><span class="sxs-lookup"><span data-stu-id="fae88-103">IWiaItem2::GetParentItem method</span></span>

<span data-ttu-id="fae88-104">Obtient l’élément parent dans l’arborescence qui représente un périphérique matériel WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="fae88-104">Gets the parent item in the tree that represents a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae88-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fae88-105">Syntax</span></span>


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="fae88-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fae88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae88-107">*ppIWiaItem2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fae88-107">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fae88-108">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fae88-108">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="fae88-109">Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) du parent de l’élément dans l’arborescence d’objets Item.</span><span class="sxs-lookup"><span data-stu-id="fae88-109">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the parent of the item in the tree of item objects.</span></span> <span data-ttu-id="fae88-110">Si cette méthode est appelée à la racine de l’arborescence, l’adresse retournée est **null**.</span><span class="sxs-lookup"><span data-stu-id="fae88-110">If this method is called on the root of the tree, then the returned address is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae88-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fae88-111">Return value</span></span>

<span data-ttu-id="fae88-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fae88-112">Type: **HRESULT**</span></span>

<span data-ttu-id="fae88-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fae88-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fae88-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fae88-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae88-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fae88-115">Remarks</span></span>

<span data-ttu-id="fae88-116">À partir de n’importe quel objet [**IWiaItem2**](-wia-iwiaitem2.md) dans l’arborescence d’objets d’un périphérique matériel WIA 2,0, l’application récupère un pointeur vers l’élément parent en appelant cette fonction.</span><span class="sxs-lookup"><span data-stu-id="fae88-116">Given any [**IWiaItem2**](-wia-iwiaitem2.md) object in the object tree of a WIA 2.0 hardware device, the application retrieves a pointer to the parent item by calling this function.</span></span>

<span data-ttu-id="fae88-117">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* si ces pointeurs ne sont pas **null**.</span><span class="sxs-lookup"><span data-stu-id="fae88-117">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter if these pointers are not **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fae88-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fae88-118">Requirements</span></span>



| <span data-ttu-id="fae88-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fae88-119">Requirement</span></span> | <span data-ttu-id="fae88-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fae88-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fae88-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fae88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fae88-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fae88-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fae88-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fae88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fae88-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fae88-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fae88-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fae88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae88-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fae88-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="fae88-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="fae88-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fae88-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fae88-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 
