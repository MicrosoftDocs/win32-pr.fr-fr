---
description: Fonction proxy pour la méthode CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320121"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="d8dbb-103">IWICImagingFactory \_ \_ fonction proxy CreateComponentInfo</span><span class="sxs-lookup"><span data-stu-id="d8dbb-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="d8dbb-104">Fonction proxy pour la méthode [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="d8dbb-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8dbb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8dbb-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d8dbb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8dbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8dbb-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8dbb-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dbb-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d8dbb-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d8dbb-109">_clsidComponent \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8dbb-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dbb-110">Type : **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="d8dbb-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="d8dbb-111">CLSID du composant souhaité.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="d8dbb-112">*ppIInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8dbb-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8dbb-113">Type : **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="d8dbb-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="d8dbb-114">Pointeur qui reçoit un pointeur vers un nouveau [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span><span class="sxs-lookup"><span data-stu-id="d8dbb-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8dbb-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8dbb-115">Return value</span></span>

<span data-ttu-id="d8dbb-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8dbb-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d8dbb-117">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8dbb-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8dbb-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8dbb-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d8dbb-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8dbb-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8dbb-120">Requirements</span></span>



| <span data-ttu-id="d8dbb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8dbb-121">Requirement</span></span> | <span data-ttu-id="d8dbb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8dbb-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8dbb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8dbb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d8dbb-124">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8dbb-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8dbb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8dbb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d8dbb-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8dbb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8dbb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d8dbb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8dbb-128"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8dbb-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




