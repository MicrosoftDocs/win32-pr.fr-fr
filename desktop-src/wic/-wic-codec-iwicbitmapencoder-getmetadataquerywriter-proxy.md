---
description: Fonction proxy pour la méthode GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b536e7c4c0553df5dae0f8e11db33c6d709e8c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519283"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="bef27-103">IWICBitmapEncoder \_ \_ fonction proxy GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="bef27-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="bef27-104">Fonction proxy pour la méthode [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="bef27-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bef27-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="bef27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bef27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef27-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bef27-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bef27-108">Tapez : \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="bef27-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="bef27-109">Pointeur vers cet objet [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="bef27-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="bef27-110">*ppIMetadataQueryWriter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bef27-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bef27-111">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="bef27-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="bef27-112">Pointeur qui reçoit un pointeur vers un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="bef27-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef27-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bef27-113">Return value</span></span>

<span data-ttu-id="bef27-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bef27-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bef27-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bef27-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bef27-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bef27-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bef27-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bef27-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bef27-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bef27-118">Requirements</span></span>



| <span data-ttu-id="bef27-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bef27-119">Requirement</span></span> | <span data-ttu-id="bef27-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="bef27-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef27-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bef27-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bef27-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bef27-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bef27-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bef27-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bef27-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bef27-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bef27-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bef27-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bef27-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bef27-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




