---
title: IMsRdpClientNonScriptable5 propriété DisableConnectionBar
description: Spécifie si le contrôle ActiveX Bureau à distance doit désactiver la barre de connexion.
ms.assetid: 82c57b93-f976-43e6-97f9-3602bf97e466
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisableConnectionBar
- Services Bureau à distance de la propriété DisableConnectionBar, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété DisableConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableConnectionBar
- IMsRdpClientNonScriptable5.put_DisableConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a129d4781db69a564eecbca3a715c3c5ccf1a9cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519234"
---
# <a name="imsrdpclientnonscriptable5disableconnectionbar-property"></a><span data-ttu-id="3731b-106">IMsRdpClientNonScriptable5 ::D propriété isableConnectionBar</span><span class="sxs-lookup"><span data-stu-id="3731b-106">IMsRdpClientNonScriptable5::DisableConnectionBar property</span></span>

<span data-ttu-id="3731b-107">Spécifie si le contrôle ActiveX Bureau à distance doit désactiver la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="3731b-107">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span> <span data-ttu-id="3731b-108">Si cette propriété contient **la \_ valeur variant true**, la barre de connexion doit être désactivée.</span><span class="sxs-lookup"><span data-stu-id="3731b-108">If this property contains **VARIANT\_TRUE**, the connection bar should be disabled.</span></span> <span data-ttu-id="3731b-109">Si cette propriété contient **la \_ valeur false**, la barre de connexion doit être activée.</span><span class="sxs-lookup"><span data-stu-id="3731b-109">If this property contains **VARIANT\_FALSE**, the connection bar should be enabled.</span></span>

<span data-ttu-id="3731b-110">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="3731b-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3731b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3731b-111">Syntax</span></span>


```C++
HRESULT put_DisableConnectionBar(
  [in] VARIANT_BOOL fDisableConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="3731b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3731b-112">Property value</span></span>

<span data-ttu-id="3731b-113">Spécifie la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3731b-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3731b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3731b-114">Requirements</span></span>



| <span data-ttu-id="3731b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3731b-115">Requirement</span></span> | <span data-ttu-id="3731b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3731b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3731b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3731b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3731b-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3731b-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3731b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3731b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3731b-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3731b-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="3731b-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3731b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="3731b-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3731b-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="3731b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3731b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3731b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3731b-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="3731b-125">IID</span><span class="sxs-lookup"><span data-stu-id="3731b-125">IID</span></span><br/>                      | <span data-ttu-id="3731b-126">IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="3731b-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3731b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3731b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3731b-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="3731b-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





