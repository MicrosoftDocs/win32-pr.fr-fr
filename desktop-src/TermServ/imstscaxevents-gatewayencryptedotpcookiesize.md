---
title: IMsRdpClientTransportSettings2 propriété GatewayEncryptedOtpCookieSize
description: Spécifie ou récupère la taille du cookie de mot de passe à usage unique chiffré.
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayEncryptedOtpCookieSize
- Services Bureau à distance de la propriété GatewayEncryptedOtpCookieSize, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayEncryptedOtpCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741340"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="e6205-106">IMsRdpClientTransportSettings2 :: GatewayEncryptedOtpCookieSize, propriété</span><span class="sxs-lookup"><span data-stu-id="e6205-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="e6205-107">Spécifie ou récupère la taille du cookie de mot de passe à usage unique chiffré.</span><span class="sxs-lookup"><span data-stu-id="e6205-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="e6205-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e6205-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6205-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6205-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="e6205-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e6205-110">Property value</span></span>

<span data-ttu-id="e6205-111">Spécifie ou récupère la taille du cookie de mot de passe à usage unique chiffré.</span><span class="sxs-lookup"><span data-stu-id="e6205-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6205-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6205-112">Requirements</span></span>



| <span data-ttu-id="e6205-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6205-113">Requirement</span></span> | <span data-ttu-id="e6205-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6205-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6205-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6205-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e6205-116">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="e6205-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="e6205-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6205-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e6205-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6205-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="e6205-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e6205-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6205-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6205-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e6205-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e6205-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6205-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6205-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e6205-123">IID</span><span class="sxs-lookup"><span data-stu-id="e6205-123">IID</span></span><br/>                      | <span data-ttu-id="e6205-124">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="e6205-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6205-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6205-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6205-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="e6205-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="e6205-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="e6205-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





