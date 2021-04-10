---
description: Remplit un tableau de pointeurs vers des interfaces IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2 :: Next, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201673"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="ac30b-103">IEnumWiaItem2 :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="ac30b-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="ac30b-104">Remplit un tableau de pointeurs vers des interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="ac30b-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac30b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac30b-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ac30b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac30b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac30b-107">*cElt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac30b-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30b-108">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="ac30b-108">Type: **ULONG**</span></span>

<span data-ttu-id="ac30b-109">Spécifie le nombre d’éléments de tableau dans le tableau indiqué par le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="ac30b-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ac30b-110">*ppIWiaItem2* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ac30b-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30b-111">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ac30b-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="ac30b-112">Reçoit l’adresse d’un tableau de pointeurs d’interface [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="ac30b-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="ac30b-113">**IEnumWiaItem2 :: Next** remplit ce tableau avec des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="ac30b-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="ac30b-114">*pcEltFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ac30b-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30b-115">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="ac30b-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="ac30b-116">Lors de la sortie, ce paramètre reçoit le nombre de pointeurs d’interface réellement stockés dans le tableau indiqué par le paramètre _ppIWiaItem2 \*.</span><span class="sxs-lookup"><span data-stu-id="ac30b-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="ac30b-117">Lorsque l’énumération est terminée, ce paramètre contient la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ac30b-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac30b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac30b-118">Return value</span></span>

<span data-ttu-id="ac30b-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac30b-119">Type: **HRESULT**</span></span>

<span data-ttu-id="ac30b-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac30b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac30b-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac30b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac30b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ac30b-122">Remarks</span></span>

<span data-ttu-id="ac30b-123">Le système d’exécution Windows Image Acquisition (WIA) 2,0 représente les périphériques matériels WIA 2,0 sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="ac30b-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="ac30b-124">Les applications utilisent la méthode **IEnumWiaItem2 :: Next** pour obtenir un pointeur d’interface **IWiaItem2** pour chaque élément dans le dossier actif de l’arborescence d’objets **IWiaItem2** d’un périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="ac30b-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="ac30b-125">Pour obtenir la liste des pointeurs, l’application passe un tableau de pointeurs d’interface [**IWiaItem2**](-wia-iwiaitem2.md) qu’il alloue.</span><span class="sxs-lookup"><span data-stu-id="ac30b-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="ac30b-126">Il passe également le nombre d’éléments de tableau dans le paramètre *cElt*.</span><span class="sxs-lookup"><span data-stu-id="ac30b-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="ac30b-127">La méthode **IEnumWiaItem2 :: Next** remplit le tableau avec des pointeurs vers des interfaces **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="ac30b-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="ac30b-128">Tant que le processus d’énumération n’est pas terminé, la méthode **IEnumWiaItem2 :: Next** retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac30b-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="ac30b-129">À chaque fois, il définit la valeur désignée par *pcEltFetched* sur le nombre d’éléments qu’il a insérés dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ac30b-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="ac30b-130">Si **IEnumWiaItem2 :: Next** termine le processus d’énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) , il retourne S \_ false et définit l’emplacement de la mémoire désigné par *pcEltFetched* à zéro.</span><span class="sxs-lookup"><span data-stu-id="ac30b-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="ac30b-131">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="ac30b-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac30b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac30b-132">Requirements</span></span>



| <span data-ttu-id="ac30b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac30b-133">Requirement</span></span> | <span data-ttu-id="ac30b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac30b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac30b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac30b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ac30b-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac30b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ac30b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac30b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ac30b-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac30b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ac30b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac30b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac30b-140"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac30b-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac30b-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="ac30b-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac30b-142"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac30b-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
