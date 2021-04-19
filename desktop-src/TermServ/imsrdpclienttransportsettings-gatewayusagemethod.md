---
title: IMsRdpClientTransportSettings propriété GatewayUsageMethod
description: Spécifie quand utiliser un serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayUsageMethod
- Services Bureau à distance de la propriété GatewayUsageMethod, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509090"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="ee9bd-106">IMsRdpClientTransportSettings :: GatewayUsageMethod, propriété</span><span class="sxs-lookup"><span data-stu-id="ee9bd-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="ee9bd-107">Spécifie quand utiliser un serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="ee9bd-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="ee9bd-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9bd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee9bd-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="ee9bd-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ee9bd-110">Property value</span></span>

<span data-ttu-id="ee9bd-111">Variable **ULong** qui spécifie la méthode d’utilisation du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="ee9bd-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="ee9bd-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Mode proxy \_ aucune \_ directe** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="ee9bd-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="ee9bd-114">N’utilisez pas de serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="ee9bd-115">Dans l’interface utilisateur du client Connexion Bureau à distance (RDC), la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="ee9bd-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Mode proxy \_ direct** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ee9bd-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ee9bd-117">Utilisez toujours un serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="ee9bd-118">Dans l’interface utilisateur du client RDC, la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="ee9bd-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Détection en mode proxy** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="ee9bd-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ee9bd-120">Utilisez un serveur de passerelle Bureau à distance s’il est impossible d’établir une connexion directe au serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="ee9bd-121">Dans l’interface utilisateur du client RDC, la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est activée.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="ee9bd-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_Mode proxy \_ par défaut** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="ee9bd-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="ee9bd-123">Utilisez les paramètres par défaut du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="ee9bd-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ \_Mode proxy \_ aucune \_ détection** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ee9bd-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ee9bd-125">N’utilisez pas de serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="ee9bd-126">Dans l’interface utilisateur du client RDC, la case à cocher **ignorer le serveur de passerelle Bureau à distance pour les adresses locales** est activée.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="ee9bd-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ee9bd-127">Error codes</span></span>

<span data-ttu-id="ee9bd-128">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="ee9bd-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee9bd-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee9bd-129">Requirements</span></span>



| <span data-ttu-id="ee9bd-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee9bd-130">Requirement</span></span> | <span data-ttu-id="ee9bd-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee9bd-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9bd-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee9bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9bd-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee9bd-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ee9bd-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee9bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9bd-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee9bd-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ee9bd-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ee9bd-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee9bd-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee9bd-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ee9bd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ee9bd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee9bd-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee9bd-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ee9bd-140">IID</span><span class="sxs-lookup"><span data-stu-id="ee9bd-140">IID</span></span><br/>                      | <span data-ttu-id="ee9bd-141">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="ee9bd-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee9bd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee9bd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9bd-143">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="ee9bd-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





