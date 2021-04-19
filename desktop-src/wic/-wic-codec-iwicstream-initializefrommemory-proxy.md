---
description: Fonction proxy pour la méthode InitializeFromMemory.
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
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545168"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="8f97e-103">IWICStream \_ \_ fonction proxy InitializeFromMemory</span><span class="sxs-lookup"><span data-stu-id="8f97e-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="8f97e-104">Fonction proxy pour la méthode [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="8f97e-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f97e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f97e-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="8f97e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f97e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f97e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8f97e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f97e-108">Tapez : \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="8f97e-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="8f97e-109">Pointeur vers cet objet [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="8f97e-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="8f97e-110">*pbBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8f97e-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f97e-111">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="8f97e-111">Type: \**BYTE\** _</span></span>

<span data-ttu-id="8f97e-112">Pointeur vers la mémoire tampon utilisée pour initialiser le flux.</span><span class="sxs-lookup"><span data-stu-id="8f97e-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="8f97e-113">_cbBufferSize \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8f97e-113">_cbBufferSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f97e-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f97e-114">Type: **DWORD**</span></span>

<span data-ttu-id="8f97e-115">Taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8f97e-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f97e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f97e-116">Return value</span></span>

<span data-ttu-id="8f97e-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8f97e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8f97e-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8f97e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f97e-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f97e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f97e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8f97e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8f97e-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8f97e-121">Requirements</span></span>



| <span data-ttu-id="8f97e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f97e-122">Requirement</span></span> | <span data-ttu-id="8f97e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f97e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f97e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f97e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8f97e-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f97e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8f97e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f97e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8f97e-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f97e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8f97e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8f97e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f97e-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f97e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




