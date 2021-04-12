---
description: Fonction proxy pour la méthode CreateQueryWriterFromBlockWriter.
ms.assetid: f941e3b1-1645-4ed6-b2c5-180cb4c43fca
title: IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c8c94b351e72fd7de367e5dd74a0c7ed62ce84f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204225"
---
# <a name="iwiccomponentfactory_createquerywriterfromblockwriter_proxy-function"></a><span data-ttu-id="cc8e2-103">IWICComponentFactory \_ \_ fonction proxy CreateQueryWriterFromBlockWriter</span><span class="sxs-lookup"><span data-stu-id="cc8e2-103">IWICComponentFactory\_CreateQueryWriterFromBlockWriter\_Proxy function</span></span>

<span data-ttu-id="cc8e2-104">Fonction proxy pour la méthode [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) .</span><span class="sxs-lookup"><span data-stu-id="cc8e2-104">Proxy function for the [**CreateQueryWriterFromBlockWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createquerywriterfromblockwriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc8e2-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateQueryWriterFromBlockWriter_Proxy(
  _In_  IWICComponentFactory    *THIS_PTR,
  _In_  IWICMetadataBlockWriter *pIBlockWriter,
  _Out_ IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="cc8e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc8e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc8e2-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc8e2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc8e2-108">Tapez : \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="cc8e2-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="cc8e2-109">Pointeur vers cet objet [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) .</span><span class="sxs-lookup"><span data-stu-id="cc8e2-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="cc8e2-110">*pIBlockWriter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc8e2-110">*pIBlockWriter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc8e2-111">Tapez : \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) \** _</span><span class="sxs-lookup"><span data-stu-id="cc8e2-111">Type: \**[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)\** _</span></span>

</dd> <dt>

<span data-ttu-id="cc8e2-112">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc8e2-112">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc8e2-113">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc8e2-113">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc8e2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc8e2-114">Return value</span></span>

<span data-ttu-id="cc8e2-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc8e2-115">Type: **HRESULT**</span></span>

<span data-ttu-id="cc8e2-116">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc8e2-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc8e2-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc8e2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc8e2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cc8e2-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8e2-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cc8e2-119">Requirements</span></span>



| <span data-ttu-id="cc8e2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc8e2-120">Requirement</span></span> | <span data-ttu-id="cc8e2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc8e2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8e2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc8e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8e2-123">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc8e2-123">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cc8e2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc8e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8e2-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc8e2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cc8e2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cc8e2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc8e2-127"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e2-127"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




