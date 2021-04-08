---
title: Classe MDM_Policy_Config01_RemoteManagement02
description: Les \_ stratégies de \_ \_ gestion à distance Config01 RemoteManagement02 de la stratégie MDM.
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- Classe MDM_Policy_Config01_RemoteManagement02
- Classe MDM_Policy_Config01_RemoteManagement02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76aa1a04735897d0b1c8f0e16572dd124b601c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843538"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a><span data-ttu-id="b3f45-105">\_Classe RemoteManagement02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="b3f45-105">MDM\_Policy\_Config01\_RemoteManagement02 class</span></span>

<span data-ttu-id="b3f45-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b3f45-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3f45-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b3f45-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3f45-108">Les \_ stratégies de \_ \_ gestion à distance Config01 RemoteManagement02 de la stratégie MDM.</span><span class="sxs-lookup"><span data-stu-id="b3f45-108">The MDM\_Policy\_Config01\_RemoteManagement02 remote management policies.</span></span>

<span data-ttu-id="b3f45-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b3f45-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f45-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3f45-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="b3f45-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b3f45-111">Members</span></span>

<span data-ttu-id="b3f45-112">La **classe \_ \_ Config01 \_ RemoteManagement02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b3f45-112">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="b3f45-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3f45-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3f45-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3f45-114">Properties</span></span>

<span data-ttu-id="b3f45-115">La **classe \_ \_ Config01 \_ RemoteManagement02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3f45-115">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b3f45-116">\_Client AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="b3f45-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-119">\_Service AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="b3f45-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="b3f45-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="b3f45-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="b3f45-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-131">\_Client AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="b3f45-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-134">\_Service AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="b3f45-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="b3f45-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="b3f45-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="b3f45-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="b3f45-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3f45-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3f45-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3f45-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3f45-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3f45-153">**ID**</span><span class="sxs-lookup"><span data-stu-id="b3f45-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3f45-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-156">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3f45-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="b3f45-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-159">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="b3f45-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-162">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="b3f45-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3f45-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="b3f45-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3f45-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3f45-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3f45-168">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3f45-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3f45-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3f45-169">Requirements</span></span>



| <span data-ttu-id="b3f45-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3f45-170">Requirement</span></span> | <span data-ttu-id="b3f45-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3f45-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f45-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f45-172">Minimum supported client</span></span><br/> | <span data-ttu-id="b3f45-173">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3f45-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3f45-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f45-174">Minimum supported server</span></span><br/> | <span data-ttu-id="b3f45-175">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3f45-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b3f45-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3f45-176">Namespace</span></span><br/>                | <span data-ttu-id="b3f45-177">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b3f45-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b3f45-178">MOF</span><span class="sxs-lookup"><span data-stu-id="b3f45-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3f45-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3f45-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3f45-180">DLL</span><span class="sxs-lookup"><span data-stu-id="b3f45-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3f45-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3f45-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

