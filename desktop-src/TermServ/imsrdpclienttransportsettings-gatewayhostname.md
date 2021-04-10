---
title: IMsRdpClientTransportSettings propriété GatewayHostname
description: Spécifie le nom d’hôte du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayHostname
- Services Bureau à distance de la propriété GatewayHostname, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayHostname
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317154"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="ad01d-106">IMsRdpClientTransportSettings :: GatewayHostname, propriété</span><span class="sxs-lookup"><span data-stu-id="ad01d-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="ad01d-107">Spécifie le nom d’hôte du serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="ad01d-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="ad01d-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ad01d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad01d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad01d-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="ad01d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ad01d-110">Property value</span></span>

<span data-ttu-id="ad01d-111">Chaîne qui contient le nom d’hôte du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ad01d-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ad01d-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ad01d-112">Error codes</span></span>

<span data-ttu-id="ad01d-113">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ad01d-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad01d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad01d-114">Requirements</span></span>



| <span data-ttu-id="ad01d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad01d-115">Requirement</span></span> | <span data-ttu-id="ad01d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad01d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad01d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad01d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad01d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad01d-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ad01d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad01d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad01d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad01d-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ad01d-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ad01d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad01d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad01d-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ad01d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ad01d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad01d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad01d-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ad01d-125">IID</span><span class="sxs-lookup"><span data-stu-id="ad01d-125">IID</span></span><br/>                      | <span data-ttu-id="ad01d-126">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="ad01d-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad01d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad01d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad01d-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="ad01d-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





