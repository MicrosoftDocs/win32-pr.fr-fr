---
description: Fonction proxy pour la méthode GetCount.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: IWICMetadataBlockReader_GetCount_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209767"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="928fe-103">\_Fonction de \_ proxy IWICMetadataBlockReader GetCount</span><span class="sxs-lookup"><span data-stu-id="928fe-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="928fe-104">Fonction proxy pour la méthode [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) .</span><span class="sxs-lookup"><span data-stu-id="928fe-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="928fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="928fe-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="928fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="928fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="928fe-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="928fe-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="928fe-108">Tapez : \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="928fe-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="928fe-109">Pointeur vers cet objet [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="928fe-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="928fe-110">*pcCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="928fe-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="928fe-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="928fe-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="928fe-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="928fe-112">Return value</span></span>

<span data-ttu-id="928fe-113">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="928fe-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="928fe-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="928fe-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="928fe-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="928fe-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="928fe-116">Notes</span><span class="sxs-lookup"><span data-stu-id="928fe-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="928fe-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="928fe-117">Requirements</span></span>



| <span data-ttu-id="928fe-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="928fe-118">Requirement</span></span> | <span data-ttu-id="928fe-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="928fe-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="928fe-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="928fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="928fe-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="928fe-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="928fe-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="928fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="928fe-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="928fe-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="928fe-124">DLL</span><span class="sxs-lookup"><span data-stu-id="928fe-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="928fe-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="928fe-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




