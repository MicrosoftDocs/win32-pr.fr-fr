---
title: Méthode SetSecurityLayer de la classe Win32_TSGeneralSetting
description: La méthode SetSecurityLayer définit la couche de sécurité.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSecurityLayer
- Services Bureau à distance de la méthode SetSecurityLayer, classe Win32_TSGeneralSetting
- Win32_TSGeneralSetting de la classe Services Bureau à distance, méthode SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942227"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="e547a-106">Méthode SetSecurityLayer de la \_ classe Win32 TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="e547a-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="e547a-107">La méthode **SetSecurityLayer** définit la couche de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e547a-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e547a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e547a-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="e547a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e547a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e547a-110">*Securitylayer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e547a-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e547a-111">Couche de sécurité à définir.</span><span class="sxs-lookup"><span data-stu-id="e547a-111">The security layer to set.</span></span> <span data-ttu-id="e547a-112">Si le niveau de chiffrement actuel est 1, la valeur 2 pour *securitylayer* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e547a-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="e547a-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Couche de sécurité RDP** (0)</span><span class="sxs-lookup"><span data-stu-id="e547a-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e547a-114">La communication entre le serveur et le client utilise le chiffrement RDP natif.</span><span class="sxs-lookup"><span data-stu-id="e547a-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="e547a-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Négocier** (1)</span><span class="sxs-lookup"><span data-stu-id="e547a-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e547a-116">La couche la plus sécurisée prise en charge par le client sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="e547a-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="e547a-117">S’il est pris en charge, SSL (TLS 1,0) sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="e547a-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="e547a-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span><span class="sxs-lookup"><span data-stu-id="e547a-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e547a-119">SSL (TLS 1,0) sera utilisé pour l’authentification du serveur, ainsi que pour le chiffrement de toutes les données transférées entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="e547a-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="e547a-120">Ce paramètre requiert que le serveur dispose d’un certificat compatible SSL.</span><span class="sxs-lookup"><span data-stu-id="e547a-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="e547a-121">Ce paramètre n’est pas compatible avec une valeur **MinEncryptionLevel** de 1.</span><span class="sxs-lookup"><span data-stu-id="e547a-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e547a-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e547a-122">Return value</span></span>

<span data-ttu-id="e547a-123">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e547a-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e547a-124">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e547a-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e547a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e547a-125">Remarks</span></span>

<span data-ttu-id="e547a-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e547a-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e547a-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e547a-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e547a-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e547a-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e547a-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e547a-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e547a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e547a-130">Requirements</span></span>



| <span data-ttu-id="e547a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e547a-131">Requirement</span></span> | <span data-ttu-id="e547a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e547a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e547a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e547a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e547a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e547a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e547a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e547a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e547a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e547a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e547a-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e547a-137">Namespace</span></span><br/>                | <span data-ttu-id="e547a-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e547a-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e547a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e547a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e547a-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e547a-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e547a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e547a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e547a-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e547a-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e547a-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e547a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e547a-144">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="e547a-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="e547a-145">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="e547a-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

