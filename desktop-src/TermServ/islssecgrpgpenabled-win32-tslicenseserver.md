---
title: Méthode IsLSSecGrpGPEnabled de la classe Win32_TSLicenseServer
description: Récupère si le groupe de sécurité \ 0034 ; du serveur de licences \ 0034 ; le paramètre de stratégie de groupe est activé sur le serveur de licences Bureau à distance.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSSecGrpGPEnabled
- Services Bureau à distance de la méthode IsLSSecGrpGPEnabled, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104302"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f9890-106">Méthode IsLSSecGrpGPEnabled de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="f9890-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f9890-107">Récupère si le paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » est activé sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f9890-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9890-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9890-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="f9890-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9890-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9890-110">*Activé* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f9890-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9890-111">Valeur booléenne qui indique si le paramètre de stratégie « Groupe de sécurité du serveur de licences » est activé.</span><span class="sxs-lookup"><span data-stu-id="f9890-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9890-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9890-112">Return value</span></span>

<span data-ttu-id="f9890-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="f9890-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f9890-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="f9890-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f9890-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f9890-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9890-116">Notes</span><span class="sxs-lookup"><span data-stu-id="f9890-116">Remarks</span></span>

<span data-ttu-id="f9890-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f9890-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f9890-118">Le paramètre de stratégie « Groupe de sécurité du serveur de licences » vous permet de spécifier les serveurs Bureau à distance hôte de session Bureau à distance qui sont autorisés à contacter le serveur de licences pour obtenir des licences d’accès client Services Bureau à distance (CAL RDS).</span><span class="sxs-lookup"><span data-stu-id="f9890-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="f9890-119">Si le paramètre de stratégie est activé sur le serveur de licences, le serveur ne répondra aux demandes de licences d’accès client aux services Bureau à distance des serveurs hôtes de session Bureau à distance dont les comptes d’ordinateur sont membres du groupe local ordinateurs Terminal Server sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="f9890-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="f9890-120">Le paramètre de stratégie se trouve dans le nœud suivant de l’éditeur d’une stratégie de groupe locale :</span><span class="sxs-lookup"><span data-stu-id="f9890-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="f9890-121">Configuration de l’ordinateur \\ modèles d’administration \\ composants Windows \\ Gestionnaire de \\ licences TS TS</span><span class="sxs-lookup"><span data-stu-id="f9890-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="f9890-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9890-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9890-123">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f9890-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9890-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f9890-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9890-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f9890-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9890-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9890-126">Requirements</span></span>



| <span data-ttu-id="f9890-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9890-127">Requirement</span></span> | <span data-ttu-id="f9890-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9890-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9890-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9890-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f9890-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9890-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f9890-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9890-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f9890-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9890-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f9890-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f9890-133">Namespace</span></span><br/>                | <span data-ttu-id="f9890-134">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f9890-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f9890-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f9890-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9890-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9890-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9890-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f9890-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9890-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9890-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9890-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9890-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9890-140">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f9890-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

