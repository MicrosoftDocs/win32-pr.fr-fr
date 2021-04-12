---
title: IMsRdpClientTransportSettings2 propriété GatewayCredSharing
description: Spécifie ou récupère le paramètre déterminant si Bureau à distance la fonctionnalité de partage des informations d’identification de la passerelle des services Bureau à distance est activée.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayCredSharing
- Services Bureau à distance de la propriété GatewayCredSharing, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464582"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="c7519-106">IMsRdpClientTransportSettings2 :: GatewayCredSharing, propriété</span><span class="sxs-lookup"><span data-stu-id="c7519-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="c7519-107">Spécifie ou récupère le paramètre déterminant si Bureau à distance la fonctionnalité de partage des informations d’identification de la passerelle des services Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="c7519-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="c7519-108">Lorsque la fonctionnalité est activée, le contrôle ActiveX Bureau à distance tente d’utiliser les mêmes informations d’identification pour s’authentifier auprès du serveur hôte de session Bureau à distance (hôte de session Bureau à distance) et au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c7519-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="c7519-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c7519-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7519-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7519-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="c7519-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c7519-111">Property value</span></span>

<span data-ttu-id="c7519-112">Si la valeur est 1, le partage des informations d’identification est activé.</span><span class="sxs-lookup"><span data-stu-id="c7519-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="c7519-113">Si la valeur est zéro, le partage des informations d’identification est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c7519-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7519-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c7519-114">Error codes</span></span>

<span data-ttu-id="c7519-115">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="c7519-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7519-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c7519-116">Remarks</span></span>

<span data-ttu-id="c7519-117">Cette propriété est utilisée par le contrôle ActiveX pour implémenter une invite unique pour le partage des informations d’identification entre le serveur hôte de session Bureau à distance et le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c7519-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="c7519-118">Le partage des informations d’identification ne prend pas en charge le partage de mot de passe basé sur le Web avec [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) ou [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span><span class="sxs-lookup"><span data-stu-id="c7519-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7519-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7519-119">Requirements</span></span>



| <span data-ttu-id="c7519-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7519-120">Requirement</span></span> | <span data-ttu-id="c7519-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7519-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7519-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7519-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7519-123">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="c7519-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="c7519-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7519-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7519-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7519-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="c7519-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c7519-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7519-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7519-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="c7519-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c7519-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7519-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7519-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="c7519-130">IID</span><span class="sxs-lookup"><span data-stu-id="c7519-130">IID</span></span><br/>                      | <span data-ttu-id="c7519-131">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="c7519-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7519-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7519-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7519-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="c7519-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="c7519-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="c7519-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





