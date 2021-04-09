---
title: IMsRdpClientTransportSettings3 propriété GatewayAuthLoginPage
description: Adresse de la page Web de connexion à utiliser pour authentifier un utilisateur.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayAuthLoginPage
- Services Bureau à distance de la propriété GatewayAuthLoginPage, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayAuthLoginPage
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106090"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="a6605-106">IMsRdpClientTransportSettings3 :: GatewayAuthLoginPage, propriété</span><span class="sxs-lookup"><span data-stu-id="a6605-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="a6605-107">Adresse de la page Web de connexion à utiliser pour authentifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a6605-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="a6605-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a6605-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6605-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6605-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="a6605-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6605-110">Property value</span></span>

<span data-ttu-id="a6605-111">Nouvelle adresse de la page Web de connexion.</span><span class="sxs-lookup"><span data-stu-id="a6605-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6605-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6605-112">Requirements</span></span>



| <span data-ttu-id="a6605-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6605-113">Requirement</span></span> | <span data-ttu-id="a6605-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6605-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6605-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6605-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a6605-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6605-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="a6605-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6605-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a6605-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6605-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a6605-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a6605-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6605-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6605-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6605-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a6605-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6605-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6605-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6605-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6605-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6605-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="a6605-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





