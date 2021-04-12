---
description: Fonction proxy pour la méthode DoesSupportMultiframe.
ms.assetid: ceee0090-ff23-4eb4-b0ea-de1d12bceef8
title: IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d148127345e77da027191114f7e411bdae564deb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112850"
---
# <a name="iwicbitmapcodecinfo_doessupportmultiframe_proxy-function"></a><span data-ttu-id="9607f-103">IWICBitmapCodecInfo \_ \_ fonction proxy DoesSupportMultiframe</span><span class="sxs-lookup"><span data-stu-id="9607f-103">IWICBitmapCodecInfo\_DoesSupportMultiframe\_Proxy function</span></span>

<span data-ttu-id="9607f-104">Fonction proxy pour la méthode [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) .</span><span class="sxs-lookup"><span data-stu-id="9607f-104">Proxy function for the [**DoesSupportMultiframe**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportmultiframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9607f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9607f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportMultiframe_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportMultiframe
);
```



## <a name="parameters"></a><span data-ttu-id="9607f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9607f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9607f-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9607f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9607f-108">Tapez : \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9607f-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="9607f-109">Pointeur vers cet objet [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="9607f-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="9607f-110">*pfSupportMultiframe* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9607f-110">*pfSupportMultiframe* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9607f-111">Type : \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="9607f-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="9607f-112">Pointeur qui reçoit _ *true*\* si le codec prend en charge les images à plusieurs frames ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="9607f-112">A pointer that receives _ *TRUE*\* if the codec supports multi frame images; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9607f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9607f-113">Return value</span></span>

<span data-ttu-id="9607f-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9607f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9607f-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9607f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9607f-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9607f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9607f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9607f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9607f-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9607f-118">Requirements</span></span>



| <span data-ttu-id="9607f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9607f-119">Requirement</span></span> | <span data-ttu-id="9607f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9607f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9607f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9607f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9607f-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9607f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9607f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9607f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9607f-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9607f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9607f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9607f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9607f-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9607f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




