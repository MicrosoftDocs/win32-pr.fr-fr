---
description: Fonction proxy pour la création du IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: WICCreateImagingFactory_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519944"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="1f2a9-103">\_Fonction proxy WICCreateImagingFactory</span><span class="sxs-lookup"><span data-stu-id="1f2a9-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="1f2a9-104">Fonction proxy pour la création du [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="1f2a9-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f2a9-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="1f2a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f2a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2a9-107">*SDKVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f2a9-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2a9-108">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="1f2a9-109">*ppIImagingFactory* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1f2a9-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2a9-110">Type : **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="1f2a9-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2a9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f2a9-111">Return value</span></span>

<span data-ttu-id="1f2a9-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-112">Type: **HRESULT**</span></span>

<span data-ttu-id="1f2a9-113">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f2a9-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f2a9-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2a9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1f2a9-115">Remarks</span></span>

<span data-ttu-id="1f2a9-116">Cette fonction est une application auxiliaire pour la création d’une fabrique WIC pour la liaison de DLL explicite, qui était nécessaire pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="1f2a9-117">Dans un usage normal, vous pouvez utiliser [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) à la place (consultez [fabriques de classes d’API WIC](./-wic-api.md#class-factories)), car cela est toujours inclus dans toutes les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2a9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f2a9-118">Requirements</span></span>



| <span data-ttu-id="1f2a9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f2a9-119">Requirement</span></span> | <span data-ttu-id="1f2a9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f2a9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2a9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f2a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2a9-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f2a9-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1f2a9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f2a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2a9-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f2a9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1f2a9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1f2a9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f2a9-126"><dt>Windowscodecs.dll ; </dt> <dt>windowscodecs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f2a9-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

