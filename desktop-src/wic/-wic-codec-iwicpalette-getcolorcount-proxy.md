---
description: Fonction proxy pour la méthode GetColorCount.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: IWICPalette_GetColorCount_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866766"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="750ae-103">IWICPalette \_ \_ fonction proxy GetColorCount</span><span class="sxs-lookup"><span data-stu-id="750ae-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="750ae-104">Fonction proxy pour la méthode [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) .</span><span class="sxs-lookup"><span data-stu-id="750ae-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="750ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="750ae-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="750ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="750ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750ae-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="750ae-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="750ae-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="750ae-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="750ae-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="750ae-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="750ae-110">*pcCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="750ae-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="750ae-111">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="750ae-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="750ae-112">Pointeur qui reçoit le nombre de couleurs dans la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="750ae-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750ae-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="750ae-113">Return value</span></span>

<span data-ttu-id="750ae-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="750ae-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="750ae-115">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="750ae-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="750ae-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="750ae-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="750ae-117">Notes</span><span class="sxs-lookup"><span data-stu-id="750ae-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="750ae-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="750ae-118">Requirements</span></span>



| <span data-ttu-id="750ae-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="750ae-119">Requirement</span></span> | <span data-ttu-id="750ae-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="750ae-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="750ae-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="750ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="750ae-122">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="750ae-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="750ae-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="750ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="750ae-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="750ae-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="750ae-125">DLL</span><span class="sxs-lookup"><span data-stu-id="750ae-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="750ae-126"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="750ae-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




