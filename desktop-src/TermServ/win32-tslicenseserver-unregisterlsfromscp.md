---
title: Méthode UnRegisterLSFromSCP de la classe Win32_TSLicenseServer
description: Supprime le serveur de licences Bureau à distance comme point de connexion de service dans Active Directory Domain Services.
ms.assetid: 3EE6F272-A99F-49EF-BDED-D8C2C641D45B
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UnRegisterLSFromSCP
- Services Bureau à distance de la méthode UnRegisterLSFromSCP, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode UnRegisterLSFromSCP
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnRegisterLSFromSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d365b0f3e64c57fba9447d8658c3a955b6e92f73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511938"
---
# <a name="unregisterlsfromscp-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="6f87e-106">Méthode UnRegisterLSFromSCP de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="6f87e-106">UnRegisterLSFromSCP method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="6f87e-107">Supprime le serveur de licences Bureau à distance comme point de connexion de service dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6f87e-107">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f87e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f87e-108">Syntax</span></span>


```mof
uint32 UnRegisterLSFromSCP();
```



## <a name="parameters"></a><span data-ttu-id="6f87e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f87e-109">Parameters</span></span>

<span data-ttu-id="6f87e-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6f87e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f87e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f87e-111">Return value</span></span>

<span data-ttu-id="6f87e-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6f87e-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6f87e-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6f87e-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6f87e-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6f87e-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f87e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6f87e-115">Remarks</span></span>

<span data-ttu-id="6f87e-116">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6f87e-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6f87e-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6f87e-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6f87e-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6f87e-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6f87e-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6f87e-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6f87e-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6f87e-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f87e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f87e-121">Requirements</span></span>



| <span data-ttu-id="6f87e-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f87e-122">Requirement</span></span> | <span data-ttu-id="6f87e-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f87e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f87e-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f87e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6f87e-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f87e-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6f87e-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f87e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6f87e-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6f87e-127">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="6f87e-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f87e-128">Namespace</span></span><br/>                | <span data-ttu-id="6f87e-129">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6f87e-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6f87e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6f87e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f87e-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f87e-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f87e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6f87e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f87e-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f87e-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f87e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f87e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f87e-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="6f87e-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

