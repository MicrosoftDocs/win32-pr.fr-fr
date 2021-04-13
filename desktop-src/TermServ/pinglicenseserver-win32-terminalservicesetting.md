---
title: Méthode PingLicenseServer de la classe Win32_TerminalServiceSetting
description: PingLicenseServer n’est plus disponible.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode PingLicenseServer
- Services Bureau à distance de la méthode PingLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384575"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="65f90-106">Méthode PingLicenseServer de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="65f90-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="65f90-107">\[**PingLicenseServer** ne peut plus être utilisé à partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="65f90-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="65f90-108">**Windows Server 2008 :** Exécute une commande ping sur le serveur de licences pour déterminer s’il s’agit d’un serveur de licences valide.</span><span class="sxs-lookup"><span data-stu-id="65f90-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f90-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65f90-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="65f90-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65f90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f90-111">*Nom du serveur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65f90-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f90-112">Nom du serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="65f90-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f90-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65f90-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="65f90-114">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="65f90-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="65f90-115">Le serveur est un serveur de licences valide.</span><span class="sxs-lookup"><span data-stu-id="65f90-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="65f90-116">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="65f90-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="65f90-117">Le serveur de licences n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="65f90-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65f90-118">Notes</span><span class="sxs-lookup"><span data-stu-id="65f90-118">Remarks</span></span>

<span data-ttu-id="65f90-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="65f90-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="65f90-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="65f90-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="65f90-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="65f90-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="65f90-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="65f90-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="65f90-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65f90-123">Requirements</span></span>



| <span data-ttu-id="65f90-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65f90-124">Requirement</span></span> | <span data-ttu-id="65f90-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="65f90-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65f90-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65f90-126">Minimum supported client</span></span><br/> | <span data-ttu-id="65f90-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65f90-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="65f90-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65f90-128">Minimum supported server</span></span><br/> | <span data-ttu-id="65f90-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65f90-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65f90-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="65f90-130">End of client support</span></span><br/>    | <span data-ttu-id="65f90-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65f90-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="65f90-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="65f90-132">End of server support</span></span><br/>    | <span data-ttu-id="65f90-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65f90-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65f90-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65f90-134">Namespace</span></span><br/>                | <span data-ttu-id="65f90-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="65f90-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="65f90-136">MOF</span><span class="sxs-lookup"><span data-stu-id="65f90-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65f90-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65f90-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="65f90-138">DLL</span><span class="sxs-lookup"><span data-stu-id="65f90-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65f90-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65f90-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f90-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65f90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f90-141">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="65f90-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

