---
description: Fonction proxy pour la méthode GetMetadataQueryWriter.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 08ebc29691432ebed7b2a1eb01eecfcd109dbd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530208"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="0e8f6-103">IWICFastMetadataEncoder \_ \_ fonction proxy GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="0e8f6-103">IWICFastMetadataEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="0e8f6-104">Fonction proxy pour la méthode [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="0e8f6-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e8f6-105">Syntax</span></span>


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="0e8f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e8f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8f6-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e8f6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8f6-108">Tapez : \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="0e8f6-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="0e8f6-109">Pointeur vers cet objet [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="0e8f6-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="0e8f6-110">*ppIMetadataQueryWriter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0e8f6-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8f6-111">Type : **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="0e8f6-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="0e8f6-112">Pointeur qui reçoit un pointeur vers le générateur de requêtes de métadonnées de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-112">A pointer that receives a pointer to the encoder's metadata query writer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8f6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e8f6-113">Return value</span></span>

<span data-ttu-id="0e8f6-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0e8f6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0e8f6-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0e8f6-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e8f6-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0e8f6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e8f6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0e8f6-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8f6-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0e8f6-118">Requirements</span></span>



| <span data-ttu-id="0e8f6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e8f6-119">Requirement</span></span> | <span data-ttu-id="0e8f6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e8f6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8f6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e8f6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e8f6-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e8f6-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0e8f6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e8f6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e8f6-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e8f6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0e8f6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0e8f6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e8f6-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e8f6-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




