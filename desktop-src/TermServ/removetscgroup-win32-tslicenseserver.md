---
title: Méthode RemoveTSCGroup de la classe Win32_TSLicenseServer
description: RemoveTSCGroup ne peut plus être utilisé à partir de Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveTSCGroup
- Services Bureau à distance de la méthode RemoveTSCGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ca693e7e98ca811ce52292fb26622b7f2174cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509386"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="2ae0a-106">Méthode RemoveTSCGroup de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="2ae0a-106">RemoveTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="2ae0a-107">\[**RemoveTSCGroup** ne peut plus être utilisé à partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="2ae0a-107">\[**RemoveTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="2ae0a-108">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-108">This method is not supported.</span></span>

<span data-ttu-id="2ae0a-109">**Windows server 2008 R2 et Windows server 2008 :** Supprime le Terminal Server groupe local ordinateurs du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-109">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae0a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ae0a-110">Syntax</span></span>


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="2ae0a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ae0a-111">Parameters</span></span>

<span data-ttu-id="2ae0a-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ae0a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ae0a-113">Return value</span></span>

<span data-ttu-id="2ae0a-114">Retourne **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="2ae0a-115">**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2ae0a-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2ae0a-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2ae0a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ae0a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2ae0a-118">Remarks</span></span>

<span data-ttu-id="2ae0a-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2ae0a-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2ae0a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2ae0a-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2ae0a-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2ae0a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2ae0a-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2ae0a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae0a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ae0a-124">Requirements</span></span>



| <span data-ttu-id="2ae0a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ae0a-125">Requirement</span></span> | <span data-ttu-id="2ae0a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ae0a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae0a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ae0a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae0a-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ae0a-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2ae0a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ae0a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae0a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ae0a-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2ae0a-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2ae0a-131">End of client support</span></span><br/>    | <span data-ttu-id="2ae0a-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ae0a-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2ae0a-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2ae0a-133">End of server support</span></span><br/>    | <span data-ttu-id="2ae0a-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ae0a-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="2ae0a-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ae0a-135">Namespace</span></span><br/>                | <span data-ttu-id="2ae0a-136">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2ae0a-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2ae0a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="2ae0a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ae0a-138"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ae0a-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ae0a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae0a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ae0a-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ae0a-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae0a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ae0a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae0a-142">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="2ae0a-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="2ae0a-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="2ae0a-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

