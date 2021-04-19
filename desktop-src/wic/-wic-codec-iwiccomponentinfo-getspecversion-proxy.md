---
description: Fonction proxy pour la méthode GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520182"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="77b77-103">IWICComponentInfo \_ \_ fonction proxy GetSpecVersion</span><span class="sxs-lookup"><span data-stu-id="77b77-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="77b77-104">Fonction proxy pour la méthode [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .</span><span class="sxs-lookup"><span data-stu-id="77b77-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="77b77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77b77-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="77b77-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77b77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77b77-107">*Ce \_ PTR* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77b77-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b77-108">Tapez : \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="77b77-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="77b77-109">Pointeur vers cet objet [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="77b77-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="77b77-110">*cchSpecVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77b77-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77b77-111">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="77b77-111">Type: **UINT**</span></span>

<span data-ttu-id="77b77-112">Taille de la mémoire tampon *wzSpecVersion* .</span><span class="sxs-lookup"><span data-stu-id="77b77-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77b77-113">*wzSpecVersion* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="77b77-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77b77-114">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="77b77-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="77b77-115">Lorsque cette méthode est retournée, contient une chaîne invarient de culture de la version de la spécification du composant.</span><span class="sxs-lookup"><span data-stu-id="77b77-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="77b77-116">Le formulaire de version est NN. NN. NN. NN.</span><span class="sxs-lookup"><span data-stu-id="77b77-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="77b77-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77b77-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77b77-118">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="77b77-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="77b77-119">Pointeur qui reçoit la longueur réelle de la version de la spécification du composant.</span><span class="sxs-lookup"><span data-stu-id="77b77-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77b77-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77b77-120">Return value</span></span>

<span data-ttu-id="77b77-121">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="77b77-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="77b77-122">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="77b77-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77b77-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77b77-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77b77-124">Notes</span><span class="sxs-lookup"><span data-stu-id="77b77-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="77b77-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="77b77-125">Requirements</span></span>



| <span data-ttu-id="77b77-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77b77-126">Requirement</span></span> | <span data-ttu-id="77b77-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="77b77-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77b77-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77b77-128">Minimum supported client</span></span><br/> | <span data-ttu-id="77b77-129">Windows XP avec SP2, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77b77-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="77b77-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77b77-130">Minimum supported server</span></span><br/> | <span data-ttu-id="77b77-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77b77-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="77b77-132">DLL</span><span class="sxs-lookup"><span data-stu-id="77b77-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77b77-133"><dt>Windowscodecs.dll ; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77b77-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




