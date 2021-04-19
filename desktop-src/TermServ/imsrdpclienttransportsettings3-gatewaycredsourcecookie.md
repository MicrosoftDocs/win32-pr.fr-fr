---
title: IMsRdpClientTransportSettings3 propriété GatewayCredSourceCookie
description: Spécifie si la source d’informations d’identification est basée sur un cookie.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayCredSourceCookie
- Services Bureau à distance de la propriété GatewayCredSourceCookie, interface IMsRdpClientTransportSettings3
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings3, propriété GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514256"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="8581c-106">IMsRdpClientTransportSettings3 :: GatewayCredSourceCookie, propriété</span><span class="sxs-lookup"><span data-stu-id="8581c-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="8581c-107">Spécifie si la source d’informations d’identification est basée sur un cookie.</span><span class="sxs-lookup"><span data-stu-id="8581c-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="8581c-108">Contient une valeur si la source d’informations d’identification est basée sur un cookie ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8581c-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="8581c-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8581c-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8581c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8581c-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="8581c-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8581c-111">Property value</span></span>

<span data-ttu-id="8581c-112">Valeur **ULong** qui spécifie si la source d’informations d’identification est basée sur un cookie.</span><span class="sxs-lookup"><span data-stu-id="8581c-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="8581c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8581c-113">Requirements</span></span>



| <span data-ttu-id="8581c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8581c-114">Requirement</span></span> | <span data-ttu-id="8581c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8581c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8581c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8581c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8581c-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8581c-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="8581c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8581c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8581c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8581c-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8581c-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8581c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="8581c-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8581c-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8581c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8581c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8581c-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8581c-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8581c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8581c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8581c-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="8581c-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





