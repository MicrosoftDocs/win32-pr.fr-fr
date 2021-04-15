---
title: IMsRdpClientNonScriptable5 propriété DisableRemoteAppCapsCheck
description: Spécifie si le contrôle ActiveX Bureau à distance ne doit pas vérifier les fonctionnalités RemoteApp du serveur.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisableRemoteAppCapsCheck
- Services Bureau à distance de la propriété DisableRemoteAppCapsCheck, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété DisableRemoteAppCapsCheck
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467022"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="59894-106">IMsRdpClientNonScriptable5 ::D propriété isableRemoteAppCapsCheck</span><span class="sxs-lookup"><span data-stu-id="59894-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="59894-107">Spécifie si le contrôle ActiveX Bureau à distance ne doit pas vérifier les fonctionnalités RemoteApp du serveur.</span><span class="sxs-lookup"><span data-stu-id="59894-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="59894-108">Si cette propriété contient **la \_ valeur variant true**, le contrôle ne doit pas vérifier les fonctionnalités RemoteApp du serveur.</span><span class="sxs-lookup"><span data-stu-id="59894-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="59894-109">Si cette propriété contient **la \_ valeur false**, le contrôle peut vérifier les fonctionnalités RemoteApp du serveur.</span><span class="sxs-lookup"><span data-stu-id="59894-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="59894-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="59894-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59894-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59894-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="59894-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="59894-112">Property value</span></span>

<span data-ttu-id="59894-113">Spécifie la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="59894-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59894-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59894-114">Requirements</span></span>



| <span data-ttu-id="59894-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59894-115">Requirement</span></span> | <span data-ttu-id="59894-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="59894-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59894-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59894-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59894-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59894-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59894-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59894-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59894-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59894-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="59894-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="59894-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="59894-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59894-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="59894-123">DLL</span><span class="sxs-lookup"><span data-stu-id="59894-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59894-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59894-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="59894-125">IID</span><span class="sxs-lookup"><span data-stu-id="59894-125">IID</span></span><br/>                      | <span data-ttu-id="59894-126">IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="59894-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59894-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59894-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59894-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="59894-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





