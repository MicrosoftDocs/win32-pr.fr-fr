---
title: Méthode AddLSToSpecifiedLicenseServerList de la classe Win32_TerminalServiceSetting
description: Ajoute le serveur de licences donné à la fin de la liste des serveurs de licences spécifiés.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddLSToSpecifiedLicenseServerList
- Services Bureau à distance de la méthode AddLSToSpecifiedLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode AddLSToSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941883"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="37ff6-106">Méthode AddLSToSpecifiedLicenseServerList de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="37ff6-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="37ff6-107">Ajoute le serveur de licences donné à la fin de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="37ff6-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ff6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37ff6-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="37ff6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37ff6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ff6-110">*LicenseServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37ff6-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ff6-111">Nom du serveur de licences à ajouter.</span><span class="sxs-lookup"><span data-stu-id="37ff6-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ff6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37ff6-112">Return value</span></span>

<span data-ttu-id="37ff6-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="37ff6-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="37ff6-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="37ff6-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="37ff6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37ff6-115">Requirements</span></span>



| <span data-ttu-id="37ff6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37ff6-116">Requirement</span></span> | <span data-ttu-id="37ff6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="37ff6-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37ff6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ff6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37ff6-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ff6-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="37ff6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37ff6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37ff6-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37ff6-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="37ff6-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37ff6-122">Namespace</span></span><br/>                | <span data-ttu-id="37ff6-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="37ff6-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="37ff6-124">MOF</span><span class="sxs-lookup"><span data-stu-id="37ff6-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37ff6-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37ff6-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="37ff6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="37ff6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ff6-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ff6-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37ff6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37ff6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37ff6-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="37ff6-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="37ff6-130">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="37ff6-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="37ff6-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="37ff6-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="37ff6-132">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="37ff6-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="37ff6-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="37ff6-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





