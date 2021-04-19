---
title: IMsRdpClientTransportSettings2 propriété GatewayUserName
description: Spécifie ou récupère le nom d’utilisateur fourni au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayUserName
- Services Bureau à distance de la propriété GatewayUserName, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayUserName
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510944"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a><span data-ttu-id="e6c3f-106">IMsRdpClientTransportSettings2 :: GatewayUserName, propriété</span><span class="sxs-lookup"><span data-stu-id="e6c3f-106">IMsRdpClientTransportSettings2::GatewayUserName property</span></span>

<span data-ttu-id="e6c3f-107">Spécifie ou récupère le nom d’utilisateur fourni au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="e6c3f-107">Specifies or retrieves the user name that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="e6c3f-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c3f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6c3f-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a><span data-ttu-id="e6c3f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e6c3f-110">Property value</span></span>

<span data-ttu-id="e6c3f-111">Nom d’utilisateur fourni pour la connexion au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-111">The user name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6c3f-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e6c3f-112">Error codes</span></span>

<span data-ttu-id="e6c3f-113">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e6c3f-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c3f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6c3f-114">Requirements</span></span>



| <span data-ttu-id="e6c3f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6c3f-115">Requirement</span></span> | <span data-ttu-id="e6c3f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6c3f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c3f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6c3f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c3f-118">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="e6c3f-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="e6c3f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6c3f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c3f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6c3f-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="e6c3f-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e6c3f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6c3f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c3f-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e6c3f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c3f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c3f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c3f-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e6c3f-125">IID</span><span class="sxs-lookup"><span data-stu-id="e6c3f-125">IID</span></span><br/>                      | <span data-ttu-id="e6c3f-126">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="e6c3f-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6c3f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6c3f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c3f-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="e6c3f-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="e6c3f-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="e6c3f-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





