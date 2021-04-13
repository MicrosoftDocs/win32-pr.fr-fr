---
description: Fonction proxy pour la méthode SetThumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484761"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="6fef3-103">IWICBitmapEncoder \_ \_ fonction proxy SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="6fef3-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="6fef3-104">Fonction proxy pour la méthode [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="6fef3-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fef3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fef3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="6fef3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fef3-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fef3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fef3-108">Tapez : \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6fef3-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="6fef3-109">Pointeur vers cet objet [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="6fef3-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6fef3-110">*pIThumbnail* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fef3-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fef3-111">Tapez : \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="6fef3-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="6fef3-112">[_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à définir comme miniature globale.</span><span class="sxs-lookup"><span data-stu-id="6fef3-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fef3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fef3-113">Return value</span></span>

<span data-ttu-id="6fef3-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6fef3-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6fef3-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fef3-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fef3-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fef3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fef3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6fef3-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6fef3-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6fef3-118">Requirements</span></span>



| <span data-ttu-id="6fef3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fef3-119">Requirement</span></span> | <span data-ttu-id="6fef3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fef3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fef3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fef3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6fef3-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fef3-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6fef3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fef3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6fef3-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fef3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6fef3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6fef3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fef3-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fef3-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




