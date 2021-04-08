---
description: Fonction proxy pour la méthode InitializeFromPalette.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: IWICPalette_InitializeFromPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868009"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="c276a-103">IWICPalette \_ \_ fonction proxy InitializeFromPalette</span><span class="sxs-lookup"><span data-stu-id="c276a-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="c276a-104">Fonction proxy pour la méthode [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) .</span><span class="sxs-lookup"><span data-stu-id="c276a-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c276a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c276a-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="c276a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c276a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c276a-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c276a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c276a-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="c276a-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="c276a-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="c276a-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="c276a-110">*pIMILPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c276a-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c276a-111">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="c276a-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="c276a-112">Pointeur désignant la palette source.</span><span class="sxs-lookup"><span data-stu-id="c276a-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c276a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c276a-113">Return value</span></span>

<span data-ttu-id="c276a-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c276a-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c276a-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c276a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c276a-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c276a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c276a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c276a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c276a-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c276a-118">Requirements</span></span>



| <span data-ttu-id="c276a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c276a-119">Requirement</span></span> | <span data-ttu-id="c276a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c276a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c276a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c276a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c276a-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c276a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c276a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c276a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c276a-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c276a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c276a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c276a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c276a-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c276a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




