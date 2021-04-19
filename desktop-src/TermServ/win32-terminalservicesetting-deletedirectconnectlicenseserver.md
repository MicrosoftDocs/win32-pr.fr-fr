---
title: Méthode DeleteDirectConnectLicenseServer de la classe Win32_TerminalServiceSetting
description: DeleteDirectConnectLicenseServer n’est plus disponible.
ms.assetid: 190316ab-b8ed-4102-8346-42603d6451e6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteDirectConnectLicenseServer
- Services Bureau à distance de la méthode DeleteDirectConnectLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode DeleteDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.DeleteDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1929ee4294040e80ec9bb633bd70d4709b3e56b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510173"
---
# <a name="deletedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="dc81b-106">Méthode DeleteDirectConnectLicenseServer de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="dc81b-106">DeleteDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="dc81b-107">\[**DeleteDirectConnectLicenseServer** ne peut plus être utilisé à partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="dc81b-107">\[**DeleteDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="dc81b-108">**Windows Server 2008 :** Supprime un serveur de licences du Registre.</span><span class="sxs-lookup"><span data-stu-id="dc81b-108">**Windows Server 2008:** Removes a license server from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc81b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc81b-109">Syntax</span></span>


```mof
uint32 DeleteDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="dc81b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc81b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc81b-111">*LicenseServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc81b-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc81b-112">Nom du serveur de licences à supprimer.</span><span class="sxs-lookup"><span data-stu-id="dc81b-112">Name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc81b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc81b-113">Return value</span></span>

<span data-ttu-id="dc81b-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="dc81b-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="dc81b-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="dc81b-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc81b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="dc81b-116">Remarks</span></span>

<span data-ttu-id="dc81b-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="dc81b-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dc81b-118">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dc81b-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dc81b-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="dc81b-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dc81b-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dc81b-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc81b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc81b-121">Requirements</span></span>



| <span data-ttu-id="dc81b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc81b-122">Requirement</span></span> | <span data-ttu-id="dc81b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc81b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc81b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc81b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc81b-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc81b-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dc81b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc81b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc81b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc81b-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc81b-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dc81b-128">End of client support</span></span><br/>    | <span data-ttu-id="dc81b-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc81b-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dc81b-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="dc81b-130">End of server support</span></span><br/>    | <span data-ttu-id="dc81b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc81b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc81b-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dc81b-132">Namespace</span></span><br/>                | <span data-ttu-id="dc81b-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="dc81b-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="dc81b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dc81b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc81b-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc81b-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc81b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dc81b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc81b-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc81b-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc81b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc81b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc81b-139">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="dc81b-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

