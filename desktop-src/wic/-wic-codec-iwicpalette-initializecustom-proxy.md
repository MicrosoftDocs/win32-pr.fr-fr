---
description: Fonction proxy pour la méthode InitializeCustom.
ms.assetid: fe742b12-5338-41b0-b90b-aec852a26518
title: IWICPalette_InitializeCustom_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeCustom_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3b64daf458a6b916f0f9e2ba23e135d6c7328a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520723"
---
# <a name="iwicpalette_initializecustom_proxy-function"></a><span data-ttu-id="f044b-103">IWICPalette \_ \_ fonction proxy InitializeCustom</span><span class="sxs-lookup"><span data-stu-id="f044b-103">IWICPalette\_InitializeCustom\_Proxy function</span></span>

<span data-ttu-id="f044b-104">Fonction proxy pour la méthode [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) .</span><span class="sxs-lookup"><span data-stu-id="f044b-104">Proxy function for the [**InitializeCustom**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializecustom) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f044b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f044b-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeCustom_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ WICColor    *pColors,
  _In_ UINT        colorCount
);
```



## <a name="parameters"></a><span data-ttu-id="f044b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f044b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f044b-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f044b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f044b-108">Tapez : \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="f044b-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="f044b-109">Pointeur vers cet objet [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="f044b-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="f044b-110">*pColors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f044b-110">*pColors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f044b-111">Tapez : \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="f044b-111">Type: \**WICColor\** _</span></span>

<span data-ttu-id="f044b-112">Pointeur vers le tableau de couleurs.</span><span class="sxs-lookup"><span data-stu-id="f044b-112">Pointer to the color array.</span></span>

</dd> <dt>

<span data-ttu-id="f044b-113">_colorCount \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f044b-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f044b-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="f044b-114">Type: **UINT**</span></span>

<span data-ttu-id="f044b-115">Nombre de couleurs dans *pColors*.</span><span class="sxs-lookup"><span data-stu-id="f044b-115">The number of colors in *pColors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f044b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f044b-116">Return value</span></span>

<span data-ttu-id="f044b-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f044b-117">Type: **HRESULT**</span></span>

<span data-ttu-id="f044b-118">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f044b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f044b-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f044b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f044b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="f044b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f044b-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f044b-121">Requirements</span></span>



| <span data-ttu-id="f044b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f044b-122">Requirement</span></span> | <span data-ttu-id="f044b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f044b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f044b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f044b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f044b-125">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f044b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f044b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f044b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f044b-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f044b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f044b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f044b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f044b-129"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f044b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




