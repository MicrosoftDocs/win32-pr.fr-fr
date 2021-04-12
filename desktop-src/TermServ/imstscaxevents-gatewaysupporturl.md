---
title: IMsRdpClientTransportSettings2 propriété GatewaySupportUrl
description: Spécifie ou récupère l’adresse Web du site qui fournit le support technique pour ce serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewaySupportUrl
- Services Bureau à distance de la propriété GatewaySupportUrl, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384163"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="2e4f8-106">IMsRdpClientTransportSettings2 :: GatewaySupportUrl, propriété</span><span class="sxs-lookup"><span data-stu-id="2e4f8-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="2e4f8-107">Spécifie ou récupère l’adresse Web du site qui fournit le support technique pour ce serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="2e4f8-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="2e4f8-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2e4f8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4f8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e4f8-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="2e4f8-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2e4f8-110">Property value</span></span>

<span data-ttu-id="2e4f8-111">Spécifie ou récupère l’adresse Web du site qui fournit le support technique pour ce serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2e4f8-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e4f8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e4f8-112">Requirements</span></span>



| <span data-ttu-id="2e4f8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e4f8-113">Requirement</span></span> | <span data-ttu-id="2e4f8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e4f8-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4f8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e4f8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4f8-116">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="2e4f8-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="2e4f8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e4f8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4f8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e4f8-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="2e4f8-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2e4f8-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e4f8-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e4f8-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="2e4f8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2e4f8-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e4f8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e4f8-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="2e4f8-123">IID</span><span class="sxs-lookup"><span data-stu-id="2e4f8-123">IID</span></span><br/>                      | <span data-ttu-id="2e4f8-124">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="2e4f8-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e4f8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e4f8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4f8-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="2e4f8-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="2e4f8-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="2e4f8-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





