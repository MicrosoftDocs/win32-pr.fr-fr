---
title: Méthode IsSecureAccessAllowed de la classe Win32_TSLicenseServer
description: Récupère une valeur indiquant si un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est autorisé à demander des licences d’accès client Services Bureau à distance (RDS \ 160 ; Cal) à partir du serveur de licences Bureau à distance.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsSecureAccessAllowed
- Services Bureau à distance de la méthode IsSecureAccessAllowed, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508550"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="1787b-106">Méthode IsSecureAccessAllowed de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="1787b-106">IsSecureAccessAllowed method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="1787b-107">Récupère une valeur qui détermine si un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) est autorisé à demander Services Bureau à distance des licences d’accès client (CAL RDS) à partir du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1787b-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1787b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1787b-108">Syntax</span></span>


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="1787b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1787b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1787b-110">*tsname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1787b-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1787b-111">Nom du serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1787b-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="1787b-112">*Autorisé* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1787b-112">*Allowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1787b-113">Valeur booléenne qui indique si le serveur hôte de session Bureau à distance est autorisé à demander des licences d’accès client aux services Bureau à distance à partir du serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="1787b-113">Boolean value that indicates whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1787b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1787b-114">Return value</span></span>

<span data-ttu-id="1787b-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="1787b-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1787b-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="1787b-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1787b-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1787b-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1787b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1787b-118">Remarks</span></span>

<span data-ttu-id="1787b-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1787b-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1787b-120">La valeur retournée est basée sur le paramètre de stratégie de groupe « Groupe de sécurité du serveur de licences » et l’appartenance au groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="1787b-120">The returned value is based on the "license server security group" group policy setting, and membership in the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

<span data-ttu-id="1787b-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1787b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1787b-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1787b-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1787b-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1787b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1787b-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1787b-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1787b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1787b-125">Requirements</span></span>



| <span data-ttu-id="1787b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1787b-126">Requirement</span></span> | <span data-ttu-id="1787b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="1787b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1787b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1787b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1787b-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1787b-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1787b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1787b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1787b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1787b-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1787b-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1787b-132">Namespace</span></span><br/>                | <span data-ttu-id="1787b-133">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1787b-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1787b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1787b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1787b-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1787b-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1787b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1787b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1787b-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1787b-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1787b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1787b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1787b-139">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="1787b-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="1787b-140">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="1787b-140">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

