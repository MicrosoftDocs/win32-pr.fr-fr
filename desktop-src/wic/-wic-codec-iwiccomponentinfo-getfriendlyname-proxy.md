---
description: Fonction proxy pour la méthode GetFriendlyName.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529310"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="29e48-103">IWICComponentInfo \_ \_ fonction proxy GetFriendlyName</span><span class="sxs-lookup"><span data-stu-id="29e48-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="29e48-104">Fonction proxy pour la méthode [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .</span><span class="sxs-lookup"><span data-stu-id="29e48-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29e48-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="29e48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29e48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e48-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29e48-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e48-108">Tapez : \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="29e48-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="29e48-109">Pointeur vers cet objet [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="29e48-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="29e48-110">*cchFriendlyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29e48-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e48-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="29e48-111">Type: **UINT**</span></span>

<span data-ttu-id="29e48-112">Taille de la mémoire tampon *wzFriendlyName* .</span><span class="sxs-lookup"><span data-stu-id="29e48-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="29e48-113">*wzFriendlyName* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="29e48-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29e48-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="29e48-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="29e48-115">Pointeur qui reçoit le nom convivial du composant.</span><span class="sxs-lookup"><span data-stu-id="29e48-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="29e48-116">La chaîne retournée est spécifique aux paramètres régionaux, 1033 par défaut.</span><span class="sxs-lookup"><span data-stu-id="29e48-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="29e48-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="29e48-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29e48-118">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="29e48-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="29e48-119">Pointeur qui reçoit la longueur réelle du nom convivial du composant.</span><span class="sxs-lookup"><span data-stu-id="29e48-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29e48-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29e48-120">Return value</span></span>

<span data-ttu-id="29e48-121">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="29e48-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="29e48-122">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="29e48-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29e48-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29e48-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29e48-124">Notes</span><span class="sxs-lookup"><span data-stu-id="29e48-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="29e48-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="29e48-125">Requirements</span></span>



| <span data-ttu-id="29e48-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29e48-126">Requirement</span></span> | <span data-ttu-id="29e48-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="29e48-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e48-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e48-128">Minimum supported client</span></span><br/> | <span data-ttu-id="29e48-129">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29e48-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="29e48-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e48-130">Minimum supported server</span></span><br/> | <span data-ttu-id="29e48-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29e48-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="29e48-132">DLL</span><span class="sxs-lookup"><span data-stu-id="29e48-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29e48-133"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29e48-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




