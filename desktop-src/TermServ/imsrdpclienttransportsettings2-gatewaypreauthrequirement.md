---
title: IMsRdpClientTransportSettings2 propriété GatewayPreAuthRequirement
description: Spécifie ou récupère le paramètre indiquant si la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance) est activée.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayPreAuthRequirement
- Services Bureau à distance de la propriété GatewayPreAuthRequirement, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509350"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="5ddf1-106">IMsRdpClientTransportSettings2 :: GatewayPreAuthRequirement, propriété</span><span class="sxs-lookup"><span data-stu-id="5ddf1-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="5ddf1-107">Spécifie ou récupère le paramètre indiquant si la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance) est activée.</span><span class="sxs-lookup"><span data-stu-id="5ddf1-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="5ddf1-108">Lorsque le mot de passe à usage unique est activé, **GatewayPreAuthRequirement** essaie d’interroger le cookie OTP à partir du magasin de cookies Internet à l’aide de la propriété [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) .</span><span class="sxs-lookup"><span data-stu-id="5ddf1-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="5ddf1-109">En cas de réussite, **GatewayPreAuthRequirement** envoie le cookie OTP au serveur pare-feu (par exemple, Microsoft Internet Security and Acceleration \[ ISA \] Server) pour la pré-authentification.</span><span class="sxs-lookup"><span data-stu-id="5ddf1-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="5ddf1-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5ddf1-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ddf1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ddf1-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="5ddf1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5ddf1-112">Property value</span></span>

<span data-ttu-id="5ddf1-113">Si la valeur est 1, la fonctionnalité de mot de passe à usage unique est activée.</span><span class="sxs-lookup"><span data-stu-id="5ddf1-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="5ddf1-114">Si la valeur est 0, la fonctionnalité de mot de passe à usage unique est désactivée.</span><span class="sxs-lookup"><span data-stu-id="5ddf1-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ddf1-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5ddf1-115">Error codes</span></span>

<span data-ttu-id="5ddf1-116">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="5ddf1-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddf1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ddf1-117">Requirements</span></span>



| <span data-ttu-id="5ddf1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ddf1-118">Requirement</span></span> | <span data-ttu-id="5ddf1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ddf1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddf1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ddf1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddf1-121">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="5ddf1-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="5ddf1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ddf1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddf1-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ddf1-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="5ddf1-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5ddf1-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ddf1-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ddf1-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5ddf1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5ddf1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ddf1-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ddf1-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5ddf1-128">IID</span><span class="sxs-lookup"><span data-stu-id="5ddf1-128">IID</span></span><br/>                      | <span data-ttu-id="5ddf1-129">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="5ddf1-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ddf1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ddf1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddf1-131">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="5ddf1-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="5ddf1-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="5ddf1-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





