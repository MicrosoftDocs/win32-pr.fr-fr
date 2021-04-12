---
title: IMsRdpClientTransportSettings2 propriété GatewayPreAuthServerAddr
description: Spécifie ou récupère l’adresse Web du serveur de pré-authentification, qui est utilisé pour la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayPreAuthServerAddr
- Services Bureau à distance de la propriété GatewayPreAuthServerAddr, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384164"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="dd12e-106">IMsRdpClientTransportSettings2 :: GatewayPreAuthServerAddr, propriété</span><span class="sxs-lookup"><span data-stu-id="dd12e-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="dd12e-107">Spécifie ou récupère l’adresse Web du serveur de pré-authentification, qui est utilisé pour la fonctionnalité de mot de passe à usage unique de la passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="dd12e-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="dd12e-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dd12e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd12e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd12e-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="dd12e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="dd12e-110">Property value</span></span>

<span data-ttu-id="dd12e-111">Adresse Web du serveur de pré-authentification ; par exemple, l’adresse Web du serveur Microsoft Internet Security and Acceleration (ISA).</span><span class="sxs-lookup"><span data-stu-id="dd12e-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="dd12e-112">Spécifiez l’adresse Web en utilisant le format «https://*hostname*. *DomainName*. com/*WebSiteName*» ou «*nom d’hôte* https://. *DomainName*. com/*WebSiteName*».</span><span class="sxs-lookup"><span data-stu-id="dd12e-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd12e-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="dd12e-113">Error codes</span></span>

<span data-ttu-id="dd12e-114">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="dd12e-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd12e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd12e-115">Requirements</span></span>



| <span data-ttu-id="dd12e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd12e-116">Requirement</span></span> | <span data-ttu-id="dd12e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd12e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd12e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd12e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd12e-119">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="dd12e-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="dd12e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd12e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd12e-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd12e-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="dd12e-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dd12e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd12e-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd12e-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="dd12e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dd12e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd12e-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd12e-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="dd12e-126">IID</span><span class="sxs-lookup"><span data-stu-id="dd12e-126">IID</span></span><br/>                      | <span data-ttu-id="dd12e-127">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="dd12e-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd12e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd12e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd12e-129">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="dd12e-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="dd12e-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="dd12e-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





