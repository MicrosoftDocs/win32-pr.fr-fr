---
title: IMsRdpClientTransportSettings propriété GatewayIsSupported
description: Spécifie si Bureau à distance passerelle (passerelle des services Bureau à distance) est prise en charge.
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayIsSupported
- Services Bureau à distance de la propriété GatewayIsSupported, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayIsSupported
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383884"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="a604f-106">IMsRdpClientTransportSettings :: GatewayIsSupported, propriété</span><span class="sxs-lookup"><span data-stu-id="a604f-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="a604f-107">Spécifie si Bureau à distance passerelle (passerelle des services Bureau à distance) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a604f-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="a604f-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a604f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a604f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a604f-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="a604f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a604f-110">Property value</span></span>

<span data-ttu-id="a604f-111">Spécifie si la passerelle des services Bureau à distance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a604f-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a604f-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a604f-112">Error codes</span></span>

<span data-ttu-id="a604f-113">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a604f-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a604f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a604f-114">Requirements</span></span>



| <span data-ttu-id="a604f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a604f-115">Requirement</span></span> | <span data-ttu-id="a604f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a604f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a604f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a604f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a604f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a604f-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a604f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a604f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a604f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a604f-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a604f-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a604f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a604f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a604f-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a604f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a604f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a604f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a604f-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a604f-125">IID</span><span class="sxs-lookup"><span data-stu-id="a604f-125">IID</span></span><br/>                      | <span data-ttu-id="a604f-126">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="a604f-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a604f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a604f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a604f-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="a604f-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





