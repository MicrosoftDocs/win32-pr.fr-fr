---
title: Interface IMsRdpClientTransportSettings
description: Gère les paramètres de transport client pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance). | Interface IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, Description
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535123"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="b68cd-106">Interface IMsRdpClientTransportSettings</span><span class="sxs-lookup"><span data-stu-id="b68cd-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="b68cd-107">Gère les paramètres de transport client pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="b68cd-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="b68cd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b68cd-108">Members</span></span>

<span data-ttu-id="b68cd-109">L’interface **IMsRdpClientTransportSettings** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b68cd-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b68cd-110">**IMsRdpClientTransportSettings** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b68cd-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="b68cd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b68cd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b68cd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b68cd-112">Properties</span></span>

<span data-ttu-id="b68cd-113">L’interface **IMsRdpClientTransportSettings** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b68cd-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="b68cd-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="b68cd-114">Property</span></span>                                                                                                          | <span data-ttu-id="b68cd-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b68cd-115">Access type</span></span>           | <span data-ttu-id="b68cd-116">Description</span><span class="sxs-lookup"><span data-stu-id="b68cd-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="b68cd-117">**GatewayCredsSource**</span><span class="sxs-lookup"><span data-stu-id="b68cd-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="b68cd-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b68cd-118">Read/write</span></span><br/> | <span data-ttu-id="b68cd-119">Méthode d’authentification du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b68cd-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="b68cd-120">**GatewayDefaultUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="b68cd-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="b68cd-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b68cd-121">Read-only</span></span><br/>  | <span data-ttu-id="b68cd-122">Méthode d’utilisation par défaut de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b68cd-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="b68cd-123">**GatewayHostname**</span><span class="sxs-lookup"><span data-stu-id="b68cd-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="b68cd-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b68cd-124">Read/write</span></span><br/> | <span data-ttu-id="b68cd-125">Nom d’hôte du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b68cd-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="b68cd-126">**GatewayIsSupported**</span><span class="sxs-lookup"><span data-stu-id="b68cd-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="b68cd-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b68cd-127">Read-only</span></span><br/>  | <span data-ttu-id="b68cd-128">Indique si la passerelle des services Bureau à distance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b68cd-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="b68cd-129">**GatewayProfileUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="b68cd-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="b68cd-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b68cd-130">Read/write</span></span><br/> | <span data-ttu-id="b68cd-131">Méthode d’utilisation du profil de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b68cd-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="b68cd-132">**GatewayUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="b68cd-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="b68cd-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b68cd-133">Read/write</span></span><br/> | <span data-ttu-id="b68cd-134">Méthode d’utilisation du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b68cd-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="b68cd-135">**GatewayUserSelectedCredsSource**</span><span class="sxs-lookup"><span data-stu-id="b68cd-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="b68cd-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b68cd-136">Read/write</span></span><br/> | <span data-ttu-id="b68cd-137">Source des informations d’identification de la passerelle Bureau à distance spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b68cd-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b68cd-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b68cd-138">Requirements</span></span>



| <span data-ttu-id="b68cd-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b68cd-139">Requirement</span></span> | <span data-ttu-id="b68cd-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="b68cd-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b68cd-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b68cd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b68cd-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b68cd-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="b68cd-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b68cd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b68cd-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b68cd-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="b68cd-145">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b68cd-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b68cd-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b68cd-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b68cd-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b68cd-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b68cd-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b68cd-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b68cd-149">IID</span><span class="sxs-lookup"><span data-stu-id="b68cd-149">IID</span></span><br/>                      | <span data-ttu-id="b68cd-150">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="b68cd-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b68cd-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b68cd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68cd-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="b68cd-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="b68cd-153">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="b68cd-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="b68cd-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="b68cd-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

