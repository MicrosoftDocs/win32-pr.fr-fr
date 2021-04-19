---
title: Méthode IsLSPublished de la classe Win32_TSLicenseServer
description: Récupère si le serveur de licences Bureau à distance est publié dans Active Directory Domain Services (AD \ 160 ; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsLSPublished
- Services Bureau à distance de la méthode IsLSPublished, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsLSPublished
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511368"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="099d0-106">Méthode IsLSPublished de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="099d0-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="099d0-107">Récupère si le serveur de licences Bureau à distance est publié dans Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="099d0-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="099d0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="099d0-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="099d0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="099d0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099d0-110">*Publié* \[ le à\]</span><span class="sxs-lookup"><span data-stu-id="099d0-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="099d0-111">Valeur booléenne qui indique si le serveur de licences est publié dans AD DS.</span><span class="sxs-lookup"><span data-stu-id="099d0-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099d0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="099d0-112">Return value</span></span>

<span data-ttu-id="099d0-113">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="099d0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="099d0-114">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="099d0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="099d0-115">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="099d0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="099d0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="099d0-116">Remarks</span></span>

<span data-ttu-id="099d0-117">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="099d0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="099d0-118">Si le serveur de licences est publié dans AD DS, il sera automatiquement détectable par Bureau à distance serveurs hôte de session Bureau à distance dans la même forêt.</span><span class="sxs-lookup"><span data-stu-id="099d0-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="099d0-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="099d0-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="099d0-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="099d0-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="099d0-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="099d0-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="099d0-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="099d0-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="099d0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="099d0-123">Requirements</span></span>



| <span data-ttu-id="099d0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="099d0-124">Requirement</span></span> | <span data-ttu-id="099d0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="099d0-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="099d0-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="099d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="099d0-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="099d0-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="099d0-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="099d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="099d0-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="099d0-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="099d0-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="099d0-130">Namespace</span></span><br/>                | <span data-ttu-id="099d0-131">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="099d0-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="099d0-132">MOF</span><span class="sxs-lookup"><span data-stu-id="099d0-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="099d0-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="099d0-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="099d0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="099d0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="099d0-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="099d0-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099d0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="099d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099d0-137">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="099d0-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

