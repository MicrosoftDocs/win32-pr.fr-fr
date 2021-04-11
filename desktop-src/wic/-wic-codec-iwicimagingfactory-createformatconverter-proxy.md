---
description: Fonction proxy pour la méthode CreateFormatConverter.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209912"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="09f26-103">IWICImagingFactory \_ \_ fonction proxy CreateFormatConverter</span><span class="sxs-lookup"><span data-stu-id="09f26-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="09f26-104">Fonction proxy pour la méthode [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="09f26-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09f26-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="09f26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09f26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f26-107">*pFactory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09f26-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f26-108">Tapez : \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="09f26-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="09f26-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09f26-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09f26-110">Type : **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="09f26-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="09f26-111">Pointeur qui reçoit un pointeur vers un nouveau [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span><span class="sxs-lookup"><span data-stu-id="09f26-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f26-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09f26-112">Return value</span></span>

<span data-ttu-id="09f26-113">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09f26-113">Type: **HRESULT**</span></span>

<span data-ttu-id="09f26-114">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="09f26-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09f26-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09f26-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f26-116">Notes</span><span class="sxs-lookup"><span data-stu-id="09f26-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="09f26-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="09f26-117">Requirements</span></span>



| <span data-ttu-id="09f26-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09f26-118">Requirement</span></span> | <span data-ttu-id="09f26-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="09f26-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f26-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09f26-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09f26-121">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09f26-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="09f26-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09f26-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09f26-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09f26-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="09f26-124">DLL</span><span class="sxs-lookup"><span data-stu-id="09f26-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09f26-125"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09f26-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




