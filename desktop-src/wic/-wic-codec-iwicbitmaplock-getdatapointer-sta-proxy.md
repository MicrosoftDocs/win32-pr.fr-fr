---
description: Fonction proxy pour la méthode GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: IWICBitmapLock_GetDataPointer_STA_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522223"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="114e8-103">\_ \_ Fonction proxy IWICBitmapLock GetDataPointer STA \_</span><span class="sxs-lookup"><span data-stu-id="114e8-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="114e8-104">Fonction proxy pour la méthode [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .</span><span class="sxs-lookup"><span data-stu-id="114e8-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="114e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="114e8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="114e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="114e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114e8-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="114e8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="114e8-108">Tapez : \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="114e8-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="114e8-109">Pointeur vers cet objet [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="114e8-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="114e8-110">*pcbBufferSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="114e8-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="114e8-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="114e8-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="114e8-112">Pointeur qui reçoit la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="114e8-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="114e8-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="114e8-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="114e8-114">Type : **Byte \* \***</span><span class="sxs-lookup"><span data-stu-id="114e8-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="114e8-115">Pointeur qui reçoit un pointeur vers le pixel supérieur gauche dans le rectangle verrouillé.</span><span class="sxs-lookup"><span data-stu-id="114e8-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114e8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="114e8-116">Return value</span></span>

<span data-ttu-id="114e8-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="114e8-117">Type: **HRESULT**</span></span>

<span data-ttu-id="114e8-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="114e8-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="114e8-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="114e8-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="114e8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="114e8-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="114e8-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="114e8-121">Requirements</span></span>



| <span data-ttu-id="114e8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="114e8-122">Requirement</span></span> | <span data-ttu-id="114e8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="114e8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114e8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="114e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="114e8-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="114e8-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="114e8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="114e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="114e8-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="114e8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="114e8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="114e8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="114e8-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="114e8-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




