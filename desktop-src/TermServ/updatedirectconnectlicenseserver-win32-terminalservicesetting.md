---
title: Méthode UpdateDirectConnectLicenseServer de la classe Win32_TerminalServiceSetting
description: UpdateDirectConnectLicenseServer n’est plus disponible.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UpdateDirectConnectLicenseServer
- Services Bureau à distance de la méthode UpdateDirectConnectLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509926"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e7137-106">Méthode UpdateDirectConnectLicenseServer de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="e7137-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e7137-107">\[**UpdateDirectConnectLicenseServer** ne peut plus être utilisé à partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="e7137-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="e7137-108">**Windows Server 2008 :** Met à jour la liste des serveurs de licences de découverte.</span><span class="sxs-lookup"><span data-stu-id="e7137-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="e7137-109">La liste de serveurs est délimitée par des points-virgules (« ; »).</span><span class="sxs-lookup"><span data-stu-id="e7137-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="e7137-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7137-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="e7137-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7137-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7137-112">*LicenseServerList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7137-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7137-113">Liste des serveurs de licences.</span><span class="sxs-lookup"><span data-stu-id="e7137-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7137-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7137-114">Return value</span></span>

<span data-ttu-id="e7137-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e7137-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e7137-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e7137-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7137-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e7137-117">Remarks</span></span>

<span data-ttu-id="e7137-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e7137-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e7137-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e7137-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e7137-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="e7137-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e7137-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e7137-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7137-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7137-122">Requirements</span></span>



| <span data-ttu-id="e7137-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7137-123">Requirement</span></span> | <span data-ttu-id="e7137-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7137-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7137-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7137-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7137-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7137-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e7137-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7137-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7137-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7137-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7137-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e7137-129">End of client support</span></span><br/>    | <span data-ttu-id="e7137-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7137-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e7137-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e7137-131">End of server support</span></span><br/>    | <span data-ttu-id="e7137-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7137-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7137-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7137-133">Namespace</span></span><br/>                | <span data-ttu-id="e7137-134">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e7137-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e7137-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e7137-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7137-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7137-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7137-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e7137-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7137-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7137-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7137-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7137-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7137-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="e7137-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

