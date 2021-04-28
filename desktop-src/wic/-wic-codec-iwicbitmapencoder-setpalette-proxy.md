---
description: IWICBitmapEncoder_SetPalette_Proxy fonction de proxy de fonction pour la méthode SetPalette.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8503698a1e91b86698ba288e56cc65e4447c906e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091177"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="0c901-103">IWICBitmapEncoder \_ \_ fonction proxy SetPalette</span><span class="sxs-lookup"><span data-stu-id="0c901-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="0c901-104">Fonction proxy pour la méthode [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="0c901-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c901-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c901-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="0c901-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c901-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c901-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c901-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c901-108">Type : **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="0c901-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="0c901-109">Pointeur vers cet objet [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="0c901-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0c901-110">*pIPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c901-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c901-111">Type : **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="0c901-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="0c901-112">[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) à utiliser comme palette globale.</span><span class="sxs-lookup"><span data-stu-id="0c901-112">The [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c901-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c901-113">Return value</span></span>

<span data-ttu-id="0c901-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c901-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0c901-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c901-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c901-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c901-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c901-117">Notes</span><span class="sxs-lookup"><span data-stu-id="0c901-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0c901-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c901-118">Requirements</span></span>



| <span data-ttu-id="0c901-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c901-119">Requirement</span></span> | <span data-ttu-id="0c901-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c901-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c901-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c901-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c901-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c901-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0c901-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c901-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c901-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c901-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0c901-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0c901-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c901-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c901-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




