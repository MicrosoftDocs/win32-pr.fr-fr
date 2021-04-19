---
description: Fonction proxy pour la méthode GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538948"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="8559e-103">IWICComponentInfo \_ GetVersion \_ proxy, fonction</span><span class="sxs-lookup"><span data-stu-id="8559e-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="8559e-104">Fonction proxy pour la méthode [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .</span><span class="sxs-lookup"><span data-stu-id="8559e-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8559e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8559e-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="8559e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8559e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8559e-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8559e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8559e-108">Tapez : \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8559e-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="8559e-109">Pointeur vers cet objet [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="8559e-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="8559e-110">*cchVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8559e-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8559e-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="8559e-111">Type: **UINT**</span></span>

<span data-ttu-id="8559e-112">Taille de la mémoire tampon *wzVersion* .</span><span class="sxs-lookup"><span data-stu-id="8559e-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8559e-113">*wzVersion* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8559e-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8559e-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8559e-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="8559e-115">Pointeur qui reçoit une chaîne indifférente de culture de la version du composant.</span><span class="sxs-lookup"><span data-stu-id="8559e-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="8559e-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8559e-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8559e-117">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="8559e-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="8559e-118">Pointeur qui reçoit la longueur réelle de la version du composant.</span><span class="sxs-lookup"><span data-stu-id="8559e-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8559e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8559e-119">Return value</span></span>

<span data-ttu-id="8559e-120">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8559e-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8559e-121">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8559e-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8559e-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8559e-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8559e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8559e-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8559e-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8559e-124">Requirements</span></span>



| <span data-ttu-id="8559e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8559e-125">Requirement</span></span> | <span data-ttu-id="8559e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8559e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8559e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8559e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8559e-128">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8559e-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8559e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8559e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8559e-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8559e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8559e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8559e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8559e-132"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8559e-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




