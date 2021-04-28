---
description: IWICStream_InitializeFromMemory_Proxy fonction de proxy de fonction pour la méthode InitializeFromMemory.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097127"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="2b440-103">IWICStream \_ \_ fonction proxy InitializeFromMemory</span><span class="sxs-lookup"><span data-stu-id="2b440-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="2b440-104">Fonction proxy pour la méthode [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="2b440-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b440-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b440-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="2b440-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b440-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b440-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b440-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b440-108">Type : **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span><span class="sxs-lookup"><span data-stu-id="2b440-108">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span></span>

<span data-ttu-id="2b440-109">Pointeur vers cet objet [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="2b440-109">Pointer to this [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="2b440-110">*pbBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b440-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b440-111">Type : **Byte \***</span><span class="sxs-lookup"><span data-stu-id="2b440-111">Type: **BYTE\***</span></span>

<span data-ttu-id="2b440-112">Pointeur vers la mémoire tampon utilisée pour initialiser le flux.</span><span class="sxs-lookup"><span data-stu-id="2b440-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="2b440-113">*cbBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2b440-113">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b440-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2b440-114">Type: **DWORD**</span></span>

<span data-ttu-id="2b440-115">Taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2b440-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b440-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2b440-116">Return value</span></span>

<span data-ttu-id="2b440-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2b440-117">Type: **HRESULT**</span></span>

<span data-ttu-id="2b440-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2b440-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b440-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b440-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b440-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2b440-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2b440-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2b440-121">Requirements</span></span>



| <span data-ttu-id="2b440-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b440-122">Requirement</span></span> | <span data-ttu-id="2b440-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b440-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b440-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b440-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b440-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b440-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2b440-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b440-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b440-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b440-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2b440-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2b440-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b440-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b440-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




