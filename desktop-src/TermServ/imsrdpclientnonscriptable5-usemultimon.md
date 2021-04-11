---
title: IMsRdpClientNonScriptable5 propriété UseMultimon
description: Spécifie si le contrôle ActiveX Bureau à distance doit utiliser plusieurs analyses.
ms.assetid: 7832E025-80F6-4B4B-9829-C2D2EF2D8C37
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété UseMultimon
- Services Bureau à distance de la propriété UseMultimon, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété UseMultimon
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.UseMultimon
- IMsRdpClientNonScriptable5.get_UseMultimon
- IMsRdpClientNonScriptable5.put_UseMultimon
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a2991ef5591176cd2508bbb6a097fecabebf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942416"
---
# <a name="imsrdpclientnonscriptable5usemultimon-property"></a><span data-ttu-id="4fff1-106">IMsRdpClientNonScriptable5 :: UseMultimon, propriété</span><span class="sxs-lookup"><span data-stu-id="4fff1-106">IMsRdpClientNonScriptable5::UseMultimon property</span></span>

<span data-ttu-id="4fff1-107">Spécifie si le contrôle ActiveX Bureau à distance doit utiliser plusieurs analyses.</span><span class="sxs-lookup"><span data-stu-id="4fff1-107">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span> <span data-ttu-id="4fff1-108">Si cette propriété contient **la \_ valeur variant true**, le contrôle utilise plusieurs analyses.</span><span class="sxs-lookup"><span data-stu-id="4fff1-108">If this property contains **VARIANT\_TRUE**, the control will use multiple monitors.</span></span> <span data-ttu-id="4fff1-109">Si cette propriété contient **la \_ valeur false**, le contrôle n’utilise pas plusieurs analyses.</span><span class="sxs-lookup"><span data-stu-id="4fff1-109">If this property contains **VARIANT\_FALSE**, the control will not use multiple monitors.</span></span>

<span data-ttu-id="4fff1-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4fff1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fff1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fff1-111">Syntax</span></span>


```C++
HRESULT put_UseMultimon(
  [in]          VARIANT_BOOL fUseMultimon
);

HRESULT get_UseMultimon(
  [out, retval] VARIANT_BOOL *pfUseMultimon
);
```



## <a name="property-value"></a><span data-ttu-id="4fff1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4fff1-112">Property value</span></span>

<span data-ttu-id="4fff1-113">Spécifie la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4fff1-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fff1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fff1-114">Requirements</span></span>



| <span data-ttu-id="4fff1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fff1-115">Requirement</span></span> | <span data-ttu-id="4fff1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fff1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fff1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fff1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4fff1-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4fff1-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4fff1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fff1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4fff1-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fff1-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="4fff1-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4fff1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fff1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fff1-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4fff1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4fff1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fff1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fff1-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="4fff1-125">IID</span><span class="sxs-lookup"><span data-stu-id="4fff1-125">IID</span></span><br/>                      | <span data-ttu-id="4fff1-126">IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="4fff1-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fff1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fff1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fff1-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4fff1-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





