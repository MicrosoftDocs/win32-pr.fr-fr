---
title: IMsRdpClientTransportSettings2 propriété GatewayEncryptedOtpCookie
description: Spécifie ou récupère le cookie de mot de passe à usage unique chiffré.
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayEncryptedOtpCookie
- Services Bureau à distance de la propriété GatewayEncryptedOtpCookie, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayEncryptedOtpCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519225"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="e9549-106">IMsRdpClientTransportSettings2 :: GatewayEncryptedOtpCookie, propriété</span><span class="sxs-lookup"><span data-stu-id="e9549-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="e9549-107">Spécifie ou récupère le cookie de mot de passe à usage unique chiffré.</span><span class="sxs-lookup"><span data-stu-id="e9549-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="e9549-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e9549-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9549-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9549-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="e9549-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e9549-110">Property value</span></span>

<span data-ttu-id="e9549-111">Spécifie ou récupère le cookie à mot de passe à usage unique chiffré.</span><span class="sxs-lookup"><span data-stu-id="e9549-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9549-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9549-112">Requirements</span></span>



| <span data-ttu-id="e9549-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9549-113">Requirement</span></span> | <span data-ttu-id="e9549-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9549-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9549-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9549-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e9549-116">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="e9549-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="e9549-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9549-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e9549-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9549-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="e9549-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e9549-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9549-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9549-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e9549-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e9549-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9549-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9549-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e9549-123">IID</span><span class="sxs-lookup"><span data-stu-id="e9549-123">IID</span></span><br/>                      | <span data-ttu-id="e9549-124">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="e9549-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9549-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9549-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9549-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="e9549-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="e9549-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="e9549-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





