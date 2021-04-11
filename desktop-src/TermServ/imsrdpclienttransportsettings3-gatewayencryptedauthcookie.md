---
title: IMsRdpClientTransportSettings3 propriété GatewayEncryptedAuthCookie
description: Cookie d’authentification chiffré.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayEncryptedAuthCookie
- Services Bureau à distance de la propriété GatewayEncryptedAuthCookie, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayEncryptedAuthCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317250"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="3f7cc-106">IMsRdpClientTransportSettings3 :: GatewayEncryptedAuthCookie, propriété</span><span class="sxs-lookup"><span data-stu-id="3f7cc-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="3f7cc-107">Cookie d’authentification chiffré.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="3f7cc-108">La taille de la propriété est spécifiée par la propriété [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .</span><span class="sxs-lookup"><span data-stu-id="3f7cc-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="3f7cc-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7cc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f7cc-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="3f7cc-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3f7cc-111">Property value</span></span>

<span data-ttu-id="3f7cc-112">Nouveau cookie d’authentification chiffré.</span><span class="sxs-lookup"><span data-stu-id="3f7cc-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7cc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f7cc-113">Requirements</span></span>



| <span data-ttu-id="3f7cc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f7cc-114">Requirement</span></span> | <span data-ttu-id="3f7cc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f7cc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7cc-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f7cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7cc-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f7cc-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="3f7cc-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f7cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7cc-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f7cc-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3f7cc-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3f7cc-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f7cc-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7cc-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f7cc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3f7cc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f7cc-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7cc-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f7cc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f7cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7cc-125">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="3f7cc-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="3f7cc-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="3f7cc-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





