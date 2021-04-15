---
title: IMsRdpClientTransportSettings3 propriété GatewayAuthCookieServerAddr
description: Adresse du serveur pour l’authentification basée sur les cookies.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayAuthCookieServerAddr
- Services Bureau à distance de la propriété GatewayAuthCookieServerAddr, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466858"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="b17f9-106">IMsRdpClientTransportSettings3 :: GatewayAuthCookieServerAddr, propriété</span><span class="sxs-lookup"><span data-stu-id="b17f9-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="b17f9-107">Adresse du serveur pour l’authentification basée sur les cookies.</span><span class="sxs-lookup"><span data-stu-id="b17f9-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="b17f9-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b17f9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17f9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b17f9-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="b17f9-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b17f9-110">Property value</span></span>

<span data-ttu-id="b17f9-111">Nouvelle adresse de serveur pour l’authentification basée sur les cookies.</span><span class="sxs-lookup"><span data-stu-id="b17f9-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="b17f9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b17f9-112">Requirements</span></span>



| <span data-ttu-id="b17f9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b17f9-113">Requirement</span></span> | <span data-ttu-id="b17f9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b17f9-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b17f9-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17f9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b17f9-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b17f9-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="b17f9-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17f9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b17f9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b17f9-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b17f9-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b17f9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="b17f9-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b17f9-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b17f9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b17f9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b17f9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b17f9-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17f9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b17f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17f9-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="b17f9-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





