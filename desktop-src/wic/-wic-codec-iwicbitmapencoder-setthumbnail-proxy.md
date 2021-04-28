---
description: IWICBitmapEncoder_SetThumbnail_Proxy fonction de proxy de fonction pour la méthode SetThumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7666fffbac7813db8021daf38ebae9c4e68c57a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100597"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="7ca25-103">IWICBitmapEncoder \_ \_ fonction proxy SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="7ca25-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="7ca25-104">Fonction proxy pour la méthode [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="7ca25-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca25-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ca25-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="7ca25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ca25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca25-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ca25-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca25-108">Type : **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="7ca25-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="7ca25-109">Pointeur vers cet objet [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="7ca25-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ca25-110">*pIThumbnail* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ca25-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca25-111">Type : **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="7ca25-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="7ca25-112">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à définir comme miniature globale.</span><span class="sxs-lookup"><span data-stu-id="7ca25-112">The [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca25-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ca25-113">Return value</span></span>

<span data-ttu-id="7ca25-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7ca25-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7ca25-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7ca25-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ca25-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ca25-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca25-117">Notes</span><span class="sxs-lookup"><span data-stu-id="7ca25-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca25-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7ca25-118">Requirements</span></span>



| <span data-ttu-id="7ca25-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ca25-119">Requirement</span></span> | <span data-ttu-id="7ca25-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ca25-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca25-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca25-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca25-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ca25-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7ca25-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ca25-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca25-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ca25-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7ca25-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ca25-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ca25-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ca25-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




