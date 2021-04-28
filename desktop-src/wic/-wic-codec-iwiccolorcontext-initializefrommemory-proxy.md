---
description: IWICColorContext_InitializeFromMemory_Proxy fonction de proxy de fonction pour la méthode InitializeFromMemory.
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
ms.openlocfilehash: e77bbcf1e430891b031b2e77bc168c33f781eacf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097217"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="6f8cd-103">IWICColorContext \_ \_ fonction proxy InitializeFromMemory</span><span class="sxs-lookup"><span data-stu-id="6f8cd-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="6f8cd-104">Fonction proxy pour la méthode [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="6f8cd-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f8cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f8cd-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="6f8cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f8cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f8cd-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f8cd-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f8cd-108">Type : **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="6f8cd-108">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

</dd> <dt>

<span data-ttu-id="6f8cd-109">*pbBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f8cd-109">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f8cd-110">Type : **const Byte \***</span><span class="sxs-lookup"><span data-stu-id="6f8cd-110">Type: **const BYTE\***</span></span>

<span data-ttu-id="6f8cd-111">Mémoire tampon utilisée pour initialiser le [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="6f8cd-111">The buffer used to initialize the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="6f8cd-112">*cbBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f8cd-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f8cd-113">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="6f8cd-113">Type: **UINT**</span></span>

<span data-ttu-id="6f8cd-114">Taille de la mémoire tampon *pbBuffer* .</span><span class="sxs-lookup"><span data-stu-id="6f8cd-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f8cd-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6f8cd-115">Return value</span></span>

<span data-ttu-id="6f8cd-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f8cd-116">Type: **HRESULT**</span></span>

<span data-ttu-id="6f8cd-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f8cd-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f8cd-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f8cd-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f8cd-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6f8cd-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6f8cd-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f8cd-120">Requirements</span></span>



| <span data-ttu-id="6f8cd-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f8cd-121">Requirement</span></span> | <span data-ttu-id="6f8cd-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f8cd-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8cd-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f8cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6f8cd-124">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f8cd-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6f8cd-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f8cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6f8cd-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6f8cd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6f8cd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8cd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f8cd-128"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f8cd-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




