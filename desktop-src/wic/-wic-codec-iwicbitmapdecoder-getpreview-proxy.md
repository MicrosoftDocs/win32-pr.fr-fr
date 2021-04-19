---
description: Fonction proxy pour la méthode GetPreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: IWICBitmapDecoder_GetPreview_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517260"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="dfa2b-103">\_Fonction de \_ proxy IWICBitmapDecoder GetPreview</span><span class="sxs-lookup"><span data-stu-id="dfa2b-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="dfa2b-104">Fonction proxy pour la méthode [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="dfa2b-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfa2b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="dfa2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfa2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa2b-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfa2b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa2b-108">Tapez : \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="dfa2b-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="dfa2b-109">Pointeur vers cet objet [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="dfa2b-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="dfa2b-110">*ppIBitmapSource* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dfa2b-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa2b-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="dfa2b-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="dfa2b-112">Pointeur qui reçoit un pointeur vers la bitmap d’aperçu si elle est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dfa2b-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa2b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfa2b-113">Return value</span></span>

<span data-ttu-id="dfa2b-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dfa2b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="dfa2b-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dfa2b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dfa2b-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dfa2b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa2b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="dfa2b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa2b-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dfa2b-118">Requirements</span></span>



| <span data-ttu-id="dfa2b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfa2b-119">Requirement</span></span> | <span data-ttu-id="dfa2b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfa2b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa2b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa2b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa2b-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfa2b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dfa2b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa2b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa2b-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfa2b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dfa2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfa2b-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfa2b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




