---
title: IMsRdpClientTransportSettings2 propriété GatewayDomain
description: Spécifie ou récupère le nom de domaine d’un utilisateur fourni au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayDomain
- Services Bureau à distance de la propriété GatewayDomain, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayDomain
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384167"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="12924-106">IMsRdpClientTransportSettings2 :: GatewayDomain, propriété</span><span class="sxs-lookup"><span data-stu-id="12924-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="12924-107">Spécifie ou récupère le nom de domaine d’un utilisateur fourni au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="12924-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="12924-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="12924-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="12924-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12924-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="12924-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="12924-110">Property value</span></span>

<span data-ttu-id="12924-111">Nom de domaine fourni pour la connexion au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="12924-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="12924-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="12924-112">Error codes</span></span>

<span data-ttu-id="12924-113">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="12924-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="12924-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12924-114">Requirements</span></span>



| <span data-ttu-id="12924-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12924-115">Requirement</span></span> | <span data-ttu-id="12924-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="12924-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12924-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12924-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12924-118">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="12924-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="12924-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12924-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12924-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12924-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="12924-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="12924-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="12924-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12924-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="12924-123">DLL</span><span class="sxs-lookup"><span data-stu-id="12924-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12924-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12924-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="12924-125">IID</span><span class="sxs-lookup"><span data-stu-id="12924-125">IID</span></span><br/>                      | <span data-ttu-id="12924-126">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="12924-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12924-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12924-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12924-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="12924-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="12924-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="12924-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





