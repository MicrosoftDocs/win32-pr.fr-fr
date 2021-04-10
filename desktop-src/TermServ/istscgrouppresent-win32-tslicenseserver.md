---
title: Méthode IsTSCGroupPresent de la classe Win32_TSLicenseServer
description: IsTSCGroupPresent ne peut plus être utilisé à partir de Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode IsTSCGroupPresent
- Services Bureau à distance de la méthode IsTSCGroupPresent, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16683b10bbfdd08812454d67ebc8ffc169b0ca0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032637"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="051ba-106">Méthode IsTSCGroupPresent de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="051ba-106">IsTSCGroupPresent method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="051ba-107">\[**IsTSCGroupPresent** ne peut plus être utilisé à partir de Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="051ba-107">\[**IsTSCGroupPresent** is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="051ba-108">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="051ba-108">This method is not supported.</span></span>

<span data-ttu-id="051ba-109">**Windows server 2008 R2 et Windows server 2008 :** Récupère si le groupe local ordinateurs Terminal Server existe sur le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="051ba-109">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="051ba-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="051ba-110">Syntax</span></span>


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a><span data-ttu-id="051ba-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="051ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="051ba-112">*Présent* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="051ba-112">*Present* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="051ba-113">Valeur booléenne qui indique si le groupe local ordinateurs Terminal Server existe.</span><span class="sxs-lookup"><span data-stu-id="051ba-113">Boolean value that indicates whether the Terminal Server Computers local group exists.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="051ba-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="051ba-114">Return value</span></span>

<span data-ttu-id="051ba-115">Retourne **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="051ba-115">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="051ba-116">**Windows server 2008 R2 et Windows server 2008 :** Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="051ba-116">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="051ba-117">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="051ba-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="051ba-118">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="051ba-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="051ba-119">Notes</span><span class="sxs-lookup"><span data-stu-id="051ba-119">Remarks</span></span>

<span data-ttu-id="051ba-120">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="051ba-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="051ba-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="051ba-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="051ba-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="051ba-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="051ba-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="051ba-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="051ba-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="051ba-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="051ba-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="051ba-125">Requirements</span></span>



| <span data-ttu-id="051ba-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="051ba-126">Requirement</span></span> | <span data-ttu-id="051ba-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="051ba-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="051ba-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="051ba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="051ba-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="051ba-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="051ba-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="051ba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="051ba-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="051ba-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="051ba-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="051ba-132">End of client support</span></span><br/>    | <span data-ttu-id="051ba-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="051ba-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="051ba-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="051ba-134">End of server support</span></span><br/>    | <span data-ttu-id="051ba-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="051ba-135">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="051ba-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="051ba-136">Namespace</span></span><br/>                | <span data-ttu-id="051ba-137">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="051ba-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="051ba-138">MOF</span><span class="sxs-lookup"><span data-stu-id="051ba-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="051ba-139"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="051ba-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="051ba-140">DLL</span><span class="sxs-lookup"><span data-stu-id="051ba-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="051ba-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="051ba-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="051ba-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="051ba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="051ba-143">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="051ba-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

