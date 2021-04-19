---
description: Fonction proxy pour la méthode GetStride.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: IWICBitmapLock_GetStride_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518853"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="33deb-103">IWICBitmapLock \_ \_ fonction proxy GetStride</span><span class="sxs-lookup"><span data-stu-id="33deb-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="33deb-104">Fonction proxy pour la méthode [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) .</span><span class="sxs-lookup"><span data-stu-id="33deb-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33deb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33deb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="33deb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33deb-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33deb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33deb-108">Tapez : \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="33deb-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="33deb-109">Pointeur vers cet objet [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="33deb-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="33deb-110">*pcbStride* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="33deb-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33deb-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="33deb-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="33deb-112">STRIDE de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="33deb-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33deb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33deb-113">Return value</span></span>

<span data-ttu-id="33deb-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="33deb-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="33deb-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33deb-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33deb-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33deb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33deb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="33deb-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="33deb-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="33deb-118">Requirements</span></span>



| <span data-ttu-id="33deb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33deb-119">Requirement</span></span> | <span data-ttu-id="33deb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="33deb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33deb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33deb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33deb-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33deb-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="33deb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33deb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33deb-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33deb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="33deb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="33deb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33deb-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33deb-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




