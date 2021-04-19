---
description: Fonction proxy pour la méthode GetCLSID.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: IWICComponentInfo_GetCLSID_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522833"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="8edb1-103">IWICComponentInfo \_ \_ fonction proxy GetCLSID</span><span class="sxs-lookup"><span data-stu-id="8edb1-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="8edb1-104">Fonction proxy pour la méthode [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) .</span><span class="sxs-lookup"><span data-stu-id="8edb1-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8edb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8edb1-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="8edb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8edb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8edb1-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8edb1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8edb1-108">Tapez : \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8edb1-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="8edb1-109">Pointeur vers cet objet [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="8edb1-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="8edb1-110">*pclsid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8edb1-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8edb1-111">Type : \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="8edb1-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="8edb1-112">Pointeur qui reçoit le CLSID du composant.</span><span class="sxs-lookup"><span data-stu-id="8edb1-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8edb1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8edb1-113">Return value</span></span>

<span data-ttu-id="8edb1-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8edb1-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8edb1-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8edb1-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8edb1-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8edb1-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8edb1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8edb1-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8edb1-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8edb1-118">Requirements</span></span>



| <span data-ttu-id="8edb1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8edb1-119">Requirement</span></span> | <span data-ttu-id="8edb1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8edb1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8edb1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8edb1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8edb1-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8edb1-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8edb1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8edb1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8edb1-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8edb1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8edb1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8edb1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8edb1-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8edb1-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




