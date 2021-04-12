---
title: IMsRdpClientTransportSettings propriété GatewayProfileUsageMethod
description: Spécifie s’il faut utiliser les paramètres par défaut de passerelle des services Bureau à distance Bureau à distance.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayProfileUsageMethod
- Services Bureau à distance de la propriété GatewayProfileUsageMethod, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayProfileUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384584"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="eab1f-106">IMsRdpClientTransportSettings :: GatewayProfileUsageMethod, propriété</span><span class="sxs-lookup"><span data-stu-id="eab1f-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="eab1f-107">Spécifie s’il faut utiliser les paramètres par défaut de passerelle des services Bureau à distance Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="eab1f-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="eab1f-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="eab1f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab1f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eab1f-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="eab1f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eab1f-110">Property value</span></span>

<span data-ttu-id="eab1f-111">Méthode d’utilisation du profil de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="eab1f-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="eab1f-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eab1f-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="eab1f-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ MODE de profil du PROXY \_ \_ \_ par défaut** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eab1f-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eab1f-114">Utilisez le mode de profil par défaut, tel que spécifié par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="eab1f-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="eab1f-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ MODE de profil du PROXY \_ \_ \_ explicite** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="eab1f-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="eab1f-116">Utilisez des paramètres explicites, comme spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eab1f-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="eab1f-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eab1f-117">Error codes</span></span>

<span data-ttu-id="eab1f-118">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="eab1f-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab1f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eab1f-119">Requirements</span></span>



| <span data-ttu-id="eab1f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eab1f-120">Requirement</span></span> | <span data-ttu-id="eab1f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eab1f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab1f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eab1f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eab1f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eab1f-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="eab1f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eab1f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eab1f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eab1f-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="eab1f-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eab1f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="eab1f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eab1f-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="eab1f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="eab1f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab1f-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eab1f-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="eab1f-130">IID</span><span class="sxs-lookup"><span data-stu-id="eab1f-130">IID</span></span><br/>                      | <span data-ttu-id="eab1f-131">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="eab1f-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eab1f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eab1f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab1f-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="eab1f-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





