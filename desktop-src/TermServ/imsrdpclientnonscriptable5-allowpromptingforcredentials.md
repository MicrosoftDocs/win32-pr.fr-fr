---
title: IMsRdpClientNonScriptable5 propriété AllowPromptingForCredentials
description: Spécifie si le contrôle ActiveX Bureau à distance peut inviter l’utilisateur à fournir des informations d’identification.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AllowPromptingForCredentials
- Services Bureau à distance de la propriété AllowPromptingForCredentials, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512213"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="297fd-106">IMsRdpClientNonScriptable5 :: AllowPromptingForCredentials, propriété</span><span class="sxs-lookup"><span data-stu-id="297fd-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="297fd-107">Spécifie si le contrôle ActiveX Bureau à distance peut inviter l’utilisateur à fournir des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="297fd-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="297fd-108">Si cette propriété contient **la \_ valeur true**, l’utilisateur peut être invité à entrer des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="297fd-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="297fd-109">Si cette propriété contient **la \_ valeur false**, l’utilisateur ne peut pas être invité à entrer ses informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="297fd-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="297fd-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="297fd-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="297fd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="297fd-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="297fd-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="297fd-112">Property value</span></span>

<span data-ttu-id="297fd-113">Spécifie la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="297fd-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="297fd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="297fd-114">Requirements</span></span>



| <span data-ttu-id="297fd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="297fd-115">Requirement</span></span> | <span data-ttu-id="297fd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="297fd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="297fd-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="297fd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="297fd-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="297fd-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="297fd-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="297fd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="297fd-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="297fd-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="297fd-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="297fd-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="297fd-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="297fd-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="297fd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="297fd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="297fd-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="297fd-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="297fd-125">IID</span><span class="sxs-lookup"><span data-stu-id="297fd-125">IID</span></span><br/>                      | <span data-ttu-id="297fd-126">IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="297fd-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="297fd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="297fd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297fd-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="297fd-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





