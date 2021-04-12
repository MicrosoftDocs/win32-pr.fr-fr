---
description: Fonction proxy pour la méthode Commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: IWICBitmapFrameEncode_Commit_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318258"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="a96d4-103">\_Fonction proxy de validation IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="a96d4-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="a96d4-104">Fonction proxy pour la méthode [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="a96d4-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a96d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a96d4-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="a96d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a96d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a96d4-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a96d4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a96d4-108">Type : \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="a96d4-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="a96d4-109">Pointeur vers cet objet [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="a96d4-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a96d4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a96d4-110">Return value</span></span>

<span data-ttu-id="a96d4-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a96d4-111">Type: **HRESULT**</span></span>

<span data-ttu-id="a96d4-112">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a96d4-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a96d4-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a96d4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a96d4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a96d4-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a96d4-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a96d4-115">Requirements</span></span>



| <span data-ttu-id="a96d4-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a96d4-116">Requirement</span></span> | <span data-ttu-id="a96d4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a96d4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a96d4-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a96d4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a96d4-119">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a96d4-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a96d4-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a96d4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a96d4-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a96d4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a96d4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a96d4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a96d4-123"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a96d4-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




