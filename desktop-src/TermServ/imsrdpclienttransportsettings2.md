---
title: Interface IMsRdpClientTransportSettings2
description: Gère les paramètres de transport client pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance). | Interface IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, Description
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106542117"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="0a85a-106">Interface IMsRdpClientTransportSettings2</span><span class="sxs-lookup"><span data-stu-id="0a85a-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="0a85a-107">Gère les paramètres de transport client pour le serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="0a85a-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="0a85a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0a85a-108">Members</span></span>

<span data-ttu-id="0a85a-109">L’interface **IMsRdpClientTransportSettings2** hérite de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span><span class="sxs-lookup"><span data-stu-id="0a85a-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="0a85a-110">**IMsRdpClientTransportSettings2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0a85a-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="0a85a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a85a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a85a-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0a85a-112">Properties</span></span>

<span data-ttu-id="0a85a-113">L’interface **IMsRdpClientTransportSettings2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0a85a-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="0a85a-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="0a85a-114">Property</span></span>                                                                                                    | <span data-ttu-id="0a85a-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0a85a-115">Access type</span></span>           | <span data-ttu-id="0a85a-116">Description</span><span class="sxs-lookup"><span data-stu-id="0a85a-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a85a-117">**GatewayCredSharing**</span><span class="sxs-lookup"><span data-stu-id="0a85a-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="0a85a-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-118">Read/write</span></span><br/> | <span data-ttu-id="0a85a-119">Indique si la fonctionnalité d’authentification unique pour la passerelle des services Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="0a85a-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="0a85a-120">**GatewayDomain**</span><span class="sxs-lookup"><span data-stu-id="0a85a-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="0a85a-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-121">Read/write</span></span><br/> | <span data-ttu-id="0a85a-122">Nom de domaine qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0a85a-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="0a85a-123">**GatewayEncryptedOtpCookie**</span><span class="sxs-lookup"><span data-stu-id="0a85a-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="0a85a-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-124">Read/write</span></span><br/> | <span data-ttu-id="0a85a-125">Cookie à mot de passe à usage unique chiffré.</span><span class="sxs-lookup"><span data-stu-id="0a85a-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="0a85a-126">**GatewayEncryptedOtpCookieSize**</span><span class="sxs-lookup"><span data-stu-id="0a85a-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="0a85a-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-127">Read/write</span></span><br/> | <span data-ttu-id="0a85a-128">Taille, en octets, du cookie à mot de passe à usage unique chiffré.</span><span class="sxs-lookup"><span data-stu-id="0a85a-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="0a85a-129">**GatewayPassword**</span><span class="sxs-lookup"><span data-stu-id="0a85a-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="0a85a-130">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="0a85a-130">Write-only</span></span><br/> | <span data-ttu-id="0a85a-131">Mot de passe fourni par l’utilisateur pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0a85a-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="0a85a-132">**GatewayPreAuthRequirement**</span><span class="sxs-lookup"><span data-stu-id="0a85a-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="0a85a-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-133">Read/write</span></span><br/> | <span data-ttu-id="0a85a-134">Indique si la fonctionnalité de mot de passe à usage unique de la passerelle des services Bureau à distance est activée.</span><span class="sxs-lookup"><span data-stu-id="0a85a-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="0a85a-135">**GatewayPreAuthServerAddr**</span><span class="sxs-lookup"><span data-stu-id="0a85a-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="0a85a-136">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-136">Read/write</span></span><br/> | <span data-ttu-id="0a85a-137">Adresse Web du serveur de pré-authentification.</span><span class="sxs-lookup"><span data-stu-id="0a85a-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="0a85a-138">**GatewaySupportUrl**</span><span class="sxs-lookup"><span data-stu-id="0a85a-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="0a85a-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-139">Read/write</span></span><br/> | <span data-ttu-id="0a85a-140">Adresse Web du site qui fournit un support technique pour le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0a85a-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="0a85a-141">**GatewayUsername**</span><span class="sxs-lookup"><span data-stu-id="0a85a-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="0a85a-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0a85a-142">Read/write</span></span><br/> | <span data-ttu-id="0a85a-143">Nom d’utilisateur qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0a85a-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="0a85a-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a85a-144">Requirements</span></span>



| <span data-ttu-id="0a85a-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a85a-145">Requirement</span></span> | <span data-ttu-id="0a85a-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a85a-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a85a-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a85a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0a85a-148">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="0a85a-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="0a85a-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a85a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0a85a-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a85a-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="0a85a-151">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0a85a-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a85a-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a85a-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0a85a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="0a85a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a85a-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a85a-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0a85a-155">IID</span><span class="sxs-lookup"><span data-stu-id="0a85a-155">IID</span></span><br/>                      | <span data-ttu-id="0a85a-156">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="0a85a-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a85a-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a85a-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a85a-158">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="0a85a-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





