---
description: Fonction proxy pour la méthode GetReaderByIndex.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: IWICMetadataBlockReader_GetReaderByIndex_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522728"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a><span data-ttu-id="7ae85-103">\_Fonction de \_ proxy IWICMetadataBlockReader GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="7ae85-103">IWICMetadataBlockReader\_GetReaderByIndex\_Proxy function</span></span>

<span data-ttu-id="7ae85-104">Fonction proxy pour la méthode [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) .</span><span class="sxs-lookup"><span data-stu-id="7ae85-104">Proxy function for the [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae85-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ae85-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a><span data-ttu-id="7ae85-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ae85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae85-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ae85-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae85-108">Tapez : \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="7ae85-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="7ae85-109">Pointeur vers cet objet [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="7ae85-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ae85-110">*nIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ae85-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae85-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="7ae85-111">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="7ae85-112">*ppIMetadataReader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ae85-112">*ppIMetadataReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae85-113">Type : **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span><span class="sxs-lookup"><span data-stu-id="7ae85-113">Type: **[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae85-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ae85-114">Return value</span></span>

<span data-ttu-id="7ae85-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7ae85-115">Type: **HRESULT**</span></span>

<span data-ttu-id="7ae85-116">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ae85-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ae85-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ae85-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae85-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7ae85-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7ae85-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ae85-119">Requirements</span></span>



| <span data-ttu-id="7ae85-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ae85-120">Requirement</span></span> | <span data-ttu-id="7ae85-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ae85-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae85-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ae85-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ae85-123">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ae85-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7ae85-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ae85-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ae85-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ae85-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7ae85-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7ae85-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ae85-127"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ae85-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




