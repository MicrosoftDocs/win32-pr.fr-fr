---
title: Méthode CreateTSCGroup de la classe Win32_TSLicenseServer
description: CreateTSCGroup ne peut plus être utilisé à partir de Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateTSCGroup
- Services Bureau à distance de la méthode CreateTSCGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode CreateTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f10db61cb02ece09d168cb462e31246e498494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843225"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f693b-106">Méthode CreateTSCGroup de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="f693b-106">CreateTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f693b-107">\[**CreateTSCGroup** ne peut plus être utilisé à partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="f693b-107">\[**CreateTSCGroup** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="f693b-108">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f693b-108">This method is not supported.</span></span>

<span data-ttu-id="f693b-109">**Windows server 2008 R2 et Windows server 2008 :** Crée le groupe local ordinateurs Terminal Server sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="f693b-109">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f693b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f693b-110">Syntax</span></span>


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a><span data-ttu-id="f693b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f693b-111">Parameters</span></span>

<span data-ttu-id="f693b-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f693b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f693b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f693b-113">Return value</span></span>

<span data-ttu-id="f693b-114">Retourne **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="f693b-114">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="f693b-115">**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="f693b-115">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f693b-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="f693b-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f693b-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f693b-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f693b-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f693b-118">Remarks</span></span>

<span data-ttu-id="f693b-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f693b-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f693b-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f693b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f693b-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f693b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f693b-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f693b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f693b-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f693b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f693b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f693b-124">Requirements</span></span>



| <span data-ttu-id="f693b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f693b-125">Requirement</span></span> | <span data-ttu-id="f693b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f693b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f693b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f693b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f693b-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f693b-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f693b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f693b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f693b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f693b-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f693b-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f693b-131">End of client support</span></span><br/>    | <span data-ttu-id="f693b-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f693b-132">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f693b-133">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f693b-133">End of server support</span></span><br/>    | <span data-ttu-id="f693b-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f693b-134">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="f693b-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f693b-135">Namespace</span></span><br/>                | <span data-ttu-id="f693b-136">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f693b-136">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f693b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f693b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f693b-138"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f693b-138"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f693b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f693b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f693b-140"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f693b-140"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f693b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f693b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f693b-142">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f693b-142">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="f693b-143">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="f693b-143">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

