---
description: Fonction proxy pour la méthode GetMimeTypes.
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: IWICBitmapCodecInfo_GetMimeTypes_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525935"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="9eb0e-103">IWICBitmapCodecInfo \_ \_ fonction proxy GetMimeTypes</span><span class="sxs-lookup"><span data-stu-id="9eb0e-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="9eb0e-104">Fonction proxy pour la méthode [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) .</span><span class="sxs-lookup"><span data-stu-id="9eb0e-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eb0e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="9eb0e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eb0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb0e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eb0e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb0e-108">Tapez : \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9eb0e-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="9eb0e-109">Pointeur vers cet objet [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="9eb0e-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9eb0e-110">*cchMimeTypes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eb0e-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb0e-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="9eb0e-111">Type: **UINT**</span></span>

<span data-ttu-id="9eb0e-112">Taille de la mémoire tampon des types MIME.</span><span class="sxs-lookup"><span data-stu-id="9eb0e-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9eb0e-113">*wzMimeTypes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9eb0e-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb0e-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="9eb0e-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="9eb0e-115">Pointeur qui reçoit les types MIME associés au codec.</span><span class="sxs-lookup"><span data-stu-id="9eb0e-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="9eb0e-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9eb0e-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb0e-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="9eb0e-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="9eb0e-118">Taille réelle de la mémoire tampon nécessaire pour récupérer tous les types MIME associés au codec.</span><span class="sxs-lookup"><span data-stu-id="9eb0e-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb0e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9eb0e-119">Return value</span></span>

<span data-ttu-id="9eb0e-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9eb0e-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9eb0e-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9eb0e-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9eb0e-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9eb0e-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb0e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9eb0e-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb0e-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9eb0e-124">Requirements</span></span>



| <span data-ttu-id="9eb0e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eb0e-125">Requirement</span></span> | <span data-ttu-id="9eb0e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eb0e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb0e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb0e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb0e-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eb0e-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9eb0e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eb0e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb0e-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eb0e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9eb0e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb0e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb0e-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb0e-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




