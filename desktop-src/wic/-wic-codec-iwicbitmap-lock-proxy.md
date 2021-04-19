---
description: Fonction proxy pour la méthode Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516861"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="6d708-103">IWICBitmap \_ \_ fonction proxy Lock</span><span class="sxs-lookup"><span data-stu-id="6d708-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="6d708-104">Fonction proxy pour la méthode [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .</span><span class="sxs-lookup"><span data-stu-id="6d708-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d708-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d708-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="6d708-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d708-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d708-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d708-108">Tapez : \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="6d708-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="6d708-109">Pointeur vers cet objet [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="6d708-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="6d708-110">*prcLock* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d708-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d708-111">Type : \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="6d708-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="6d708-112">Rectangle auquel accéder.</span><span class="sxs-lookup"><span data-stu-id="6d708-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="6d708-113">_flags \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d708-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d708-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6d708-114">Type: **DWORD**</span></span>

<span data-ttu-id="6d708-115">Mode d’accès que vous souhaitez obtenir pour le verrou.</span><span class="sxs-lookup"><span data-stu-id="6d708-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="6d708-116">*ppILock* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6d708-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d708-117">Type : **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="6d708-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="6d708-118">Pointeur qui reçoit l’emplacement de mémoire verrouillée.</span><span class="sxs-lookup"><span data-stu-id="6d708-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d708-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d708-119">Return value</span></span>

<span data-ttu-id="6d708-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d708-120">Type: **HRESULT**</span></span>

<span data-ttu-id="6d708-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6d708-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d708-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d708-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d708-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6d708-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6d708-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d708-124">Requirements</span></span>



| <span data-ttu-id="6d708-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d708-125">Requirement</span></span> | <span data-ttu-id="6d708-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d708-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d708-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d708-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d708-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d708-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6d708-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d708-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d708-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d708-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6d708-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6d708-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d708-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d708-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




