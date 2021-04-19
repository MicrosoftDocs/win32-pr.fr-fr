---
description: Fonction proxy pour la méthode InitializeFromMemory.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518318"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="750f5-103">IWICColorContext \_ \_ fonction proxy InitializeFromMemory</span><span class="sxs-lookup"><span data-stu-id="750f5-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="750f5-104">Fonction proxy pour la méthode [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="750f5-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="750f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="750f5-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="750f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="750f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750f5-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="750f5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="750f5-108">Tapez : \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _</span><span class="sxs-lookup"><span data-stu-id="750f5-108">Type: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\** _</span></span>

</dd> <dt>

<span data-ttu-id="750f5-109">_pbBuffer \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="750f5-109">_pbBuffer\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="750f5-110">Type : \**const Byte \** _</span><span class="sxs-lookup"><span data-stu-id="750f5-110">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="750f5-111">Mémoire tampon utilisée pour initialiser le [_ *IWICColorContext* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="750f5-111">The buffer used to initialize the [_ *IWICColorContext*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="750f5-112">*cbBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="750f5-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="750f5-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="750f5-113">Type: **UINT**</span></span>

<span data-ttu-id="750f5-114">Taille de la mémoire tampon *pbBuffer* .</span><span class="sxs-lookup"><span data-stu-id="750f5-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750f5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="750f5-115">Return value</span></span>

<span data-ttu-id="750f5-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="750f5-116">Type: **HRESULT**</span></span>

<span data-ttu-id="750f5-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="750f5-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="750f5-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="750f5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="750f5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="750f5-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="750f5-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="750f5-120">Requirements</span></span>



| <span data-ttu-id="750f5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="750f5-121">Requirement</span></span> | <span data-ttu-id="750f5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="750f5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="750f5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="750f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="750f5-124">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="750f5-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="750f5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="750f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="750f5-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="750f5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="750f5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="750f5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="750f5-128"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="750f5-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




