---
description: Recherche dans l’arborescence d’un élément des sous-éléments en utilisant le nom comme clé de recherche.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: 'IWiaItem2 :: FindItemByName, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 821be7e4abd8d1396befa886093aa197bcdea7f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517526"
---
# <a name="iwiaitem2finditembyname-method"></a><span data-ttu-id="7a395-103">IWiaItem2 :: FindItemByName, méthode</span><span class="sxs-lookup"><span data-stu-id="7a395-103">IWiaItem2::FindItemByName method</span></span>

<span data-ttu-id="7a395-104">Recherche dans l’arborescence d’un élément des sous-éléments en utilisant le nom comme clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="7a395-104">Searches an item's tree of subitems using the name as the search key.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a395-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a395-105">Syntax</span></span>


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="7a395-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a395-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a395-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a395-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="7a395-108">Type: **LONG**</span></span>

<span data-ttu-id="7a395-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="7a395-109">Currently unused.</span></span> <span data-ttu-id="7a395-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="7a395-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="7a395-111">*bstrFullItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a395-111">*bstrFullItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a395-112">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a395-112">Type: **BSTR**</span></span>

<span data-ttu-id="7a395-113">Spécifie le nom de l’élément à rechercher.</span><span class="sxs-lookup"><span data-stu-id="7a395-113">Specifies the name fo the item to search for.</span></span>

</dd> <dt>

<span data-ttu-id="7a395-114">*ppIWiaItem2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7a395-114">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a395-115">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7a395-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="7a395-116">Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément trouvé.</span><span class="sxs-lookup"><span data-stu-id="7a395-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item found.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a395-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a395-117">Return value</span></span>

<span data-ttu-id="7a395-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7a395-118">Type: **HRESULT**</span></span>

<span data-ttu-id="7a395-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7a395-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7a395-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a395-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a395-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7a395-121">Remarks</span></span>

<span data-ttu-id="7a395-122">Cette méthode recherche l’arborescence des sous-éléments de l’élément actuel en utilisant le nom comme clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="7a395-122">This method searches the current item's tree of sub-items using the name as the search key.</span></span> <span data-ttu-id="7a395-123">Si **IWiaItem2 :: FindItemByName** trouve l’élément spécifié par *bstrFullItemName*, il stocke l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément dans le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="7a395-123">If **IWiaItem2::FindItemByName** finds the item specified by *bstrFullItemName*, it stores the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="7a395-124">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="7a395-124">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a395-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a395-125">Requirements</span></span>



| <span data-ttu-id="7a395-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a395-126">Requirement</span></span> | <span data-ttu-id="7a395-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a395-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a395-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a395-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7a395-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a395-129">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7a395-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a395-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7a395-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a395-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a395-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a395-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a395-133"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a395-133"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a395-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="7a395-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a395-135"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a395-135"><dt>Wia.idl</dt></span></span> </dl> |



 

 
