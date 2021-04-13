---
title: Constantes Authentication-Service (rpcdce. h)
description: Les constantes de service d’authentification représentent les services d’authentification passés à différentes fonctions d’exécution.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509206"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="24bda-103">Constantes Authentication-Service</span><span class="sxs-lookup"><span data-stu-id="24bda-103">Authentication-Service Constants</span></span>

<span data-ttu-id="24bda-104">Les constantes de service d’authentification représentent les services d’authentification passés à différentes fonctions d’exécution.</span><span class="sxs-lookup"><span data-stu-id="24bda-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="24bda-105">Les constantes suivantes sont des valeurs valides pour le paramètre *AuthnSvc* .</span><span class="sxs-lookup"><span data-stu-id="24bda-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="24bda-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="24bda-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="24bda-107">Description</span><span class="sxs-lookup"><span data-stu-id="24bda-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="24bda-108"><dt>**RPC \_ C \_ Authn \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="24bda-109">Aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="24bda-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="24bda-110"><dt>**RPC \_ C \_ Authn \_ DCE \_ privé**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="24bda-111">Utilisez l’authentification par clé privée DCE (Distributed Computing Environment).</span><span class="sxs-lookup"><span data-stu-id="24bda-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="24bda-112"><dt>**RPC \_ C \_ Authn \_ DCE \_ public**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="24bda-113">Authentification par clé publique DCE (réservée à une utilisation ultérieure).</span><span class="sxs-lookup"><span data-stu-id="24bda-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="24bda-114"><dt>**RPC \_ C \_ Authn \_ Dec \_ public**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="24bda-115">Authentification par clé publique DEC (réservée à une utilisation ultérieure).</span><span class="sxs-lookup"><span data-stu-id="24bda-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="24bda-116"><dt>**RPC \_ C \_ Authn \_ GSS \_ Negotiate**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="24bda-117">Utilisez le [SSP Microsoft Negotiate](/windows/desktop/SecAuthN/microsoft-negotiate).</span><span class="sxs-lookup"><span data-stu-id="24bda-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="24bda-118">Ce SSP négocie entre l’utilisation des fournisseurs SSP (Security Support Provider) NTLM et Kerberos.</span><span class="sxs-lookup"><span data-stu-id="24bda-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="24bda-119"><dt>**RPC \_ C \_ Authn \_ winnt**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="24bda-120">Utilisez le [SSP Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).</span><span class="sxs-lookup"><span data-stu-id="24bda-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="24bda-121"><dt>**RPC \_ C \_ Authn \_ GSS \_ Schannel**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="24bda-122">Utilisez le [SSP Schannel](/windows/desktop/SecAuthN/secure-channel).</span><span class="sxs-lookup"><span data-stu-id="24bda-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="24bda-123">Ce fournisseur de services partagés prend en charge le protocole SSL (Secure Socket Layer), PCT (Private Communication Technology) et TLS (Transport Level Security).</span><span class="sxs-lookup"><span data-stu-id="24bda-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="24bda-124"><dt>**RPC \_ C \_ Authn \_ GSS \_ Kerberos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="24bda-125">Utilisez le [SSP Microsoft Kerberos](/windows/desktop/SecAuthN/microsoft-kerberos).</span><span class="sxs-lookup"><span data-stu-id="24bda-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="24bda-126"><dt>**RPC \_ C \_ Authn \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="24bda-127">Utilisez l’authentification par mot de passe distribué (DPA).</span><span class="sxs-lookup"><span data-stu-id="24bda-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="24bda-128"><dt>**RPC \_ C \_ Authn \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="24bda-129">Protocole SSP du protocole d’authentification utilisé pour Microsoft Network (MSN).</span><span class="sxs-lookup"><span data-stu-id="24bda-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="24bda-130"><dt>**RPC \_ C \_ Authn \_ Digest**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="24bda-131">Windows XP ou version ultérieure : utiliser le [SSP Microsoft Digest](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="24bda-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="24bda-132"><dt>**RPC \_ C \_ Authn \_ Nego \_ Extender**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="24bda-133">Windows 7 ou version ultérieure : réservé.</span><span class="sxs-lookup"><span data-stu-id="24bda-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="24bda-134">À ne pas utiliser</span><span class="sxs-lookup"><span data-stu-id="24bda-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="24bda-135"><dt>**RPC \_ C \_ Authn \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="24bda-136">Ce fournisseur de services partagés fournit un wrapper compatible SSPI pour le protocole de niveau transport MSMQ (Microsoft Message Queue).</span><span class="sxs-lookup"><span data-stu-id="24bda-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="24bda-137"><dt>**RPC \_ C \_ Authn \_ par défaut**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="24bda-138">Utilisez le service d’authentification par défaut.</span><span class="sxs-lookup"><span data-stu-id="24bda-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="24bda-139">Notes</span><span class="sxs-lookup"><span data-stu-id="24bda-139">Remarks</span></span>

<span data-ttu-id="24bda-140">Spécifiez RPC \_ C \_ Authn \_ None pour désactiver l’authentification pour les appels de procédure distante effectués sur un handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="24bda-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="24bda-141">Lorsque vous spécifiez \_ \_ \_ la valeur par défaut RPC c Authn, la bibliothèque Runtime RPC utilise \_ le \_ \_ service d’authentification Winnt RPC c Authn pour les appels de procédure distante effectués à l’aide du handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="24bda-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="24bda-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24bda-142">Requirements</span></span>



| <span data-ttu-id="24bda-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24bda-143">Requirement</span></span> | <span data-ttu-id="24bda-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="24bda-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="24bda-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24bda-145">Minimum supported client</span></span><br/> | <span data-ttu-id="24bda-146">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24bda-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="24bda-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24bda-147">Minimum supported server</span></span><br/> | <span data-ttu-id="24bda-148">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24bda-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="24bda-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="24bda-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="24bda-150"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="24bda-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24bda-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24bda-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24bda-152">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="24bda-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="24bda-153">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="24bda-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="24bda-154">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="24bda-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="24bda-155">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="24bda-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="24bda-156">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="24bda-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="24bda-157">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="24bda-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

