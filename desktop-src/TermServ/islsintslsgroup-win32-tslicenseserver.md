---
title: Méthode IsLSinTSLSGroup de la classe Win32_TSLicenseServer
description: Récupère si le Bureau à distance serveur de licences est membre du groupe de serveurs de licences Bureau à distance sur un contrôleur de domaine dans un domaine donné.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSinTSLSGroup
- Services Bureau à distance de la méthode IsLSinTSLSGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511952"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="9a4a9-106">Méthode IsLSinTSLSGroup de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="9a4a9-106">IsLSinTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="9a4a9-107">Récupère si le Bureau à distance serveur de licences est membre du groupe de serveurs de licences Bureau à distance sur un contrôleur de domaine dans un domaine donné.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-107">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop license server group on a domain controller in a given domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a4a9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a4a9-108">Syntax</span></span>


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="9a4a9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a4a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a4a9-110">*Domaine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a4a9-110">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a4a9-111">Nom du domaine.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-111">The domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9a4a9-112">*IsMember* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a4a9-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a4a9-113">Valeur booléenne qui indique si le serveur de licences est membre du groupe de serveurs de licences Bureau à distance dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-113">Boolean value that indicates whether the license server is a member of the Remote Desktop license server group in the domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a4a9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a4a9-114">Return value</span></span>

<span data-ttu-id="9a4a9-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9a4a9-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9a4a9-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9a4a9-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a4a9-118">Notes</span><span class="sxs-lookup"><span data-stu-id="9a4a9-118">Remarks</span></span>

<span data-ttu-id="9a4a9-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9a4a9-120">Si aucun nom de domaine n’est fourni, un contrôleur de domaine dans le même domaine que le serveur de licences est interrogé.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-120">If no domain name is provided, a domain controller in the same domain as the license server is queried.</span></span>

<span data-ttu-id="9a4a9-121">Le serveur de licences doit être membre du groupe de serveurs de licences Bureau à distance si le serveur est configuré pour utiliser l’étendue de la découverte du domaine ou de la forêt.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-121">The license server should be a member of the Remote Desktop license server group if the server is configured to use the domain or forest discovery scope.</span></span> <span data-ttu-id="9a4a9-122">Si le serveur de licences n’est pas membre de ce groupe, le suivi des licences par utilisateur et la création de rapports ne fonctionneront pas.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-122">If the license server is not a member of this group, per-user license tracking and reporting will not work.</span></span>

<span data-ttu-id="9a4a9-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9a4a9-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9a4a9-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9a4a9-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9a4a9-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9a4a9-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9a4a9-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a4a9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a4a9-127">Requirements</span></span>



| <span data-ttu-id="9a4a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a4a9-128">Requirement</span></span> | <span data-ttu-id="9a4a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a4a9-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4a9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a4a9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a4a9-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a4a9-131">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="9a4a9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a4a9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a4a9-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a4a9-133">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="9a4a9-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9a4a9-134">Namespace</span></span><br/>                | <span data-ttu-id="9a4a9-135">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9a4a9-135">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="9a4a9-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9a4a9-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a4a9-137"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a4a9-137"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a4a9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9a4a9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a4a9-139"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a4a9-139"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a4a9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a4a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4a9-141">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9a4a9-141">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="9a4a9-142">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="9a4a9-142">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="9a4a9-143">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="9a4a9-143">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

