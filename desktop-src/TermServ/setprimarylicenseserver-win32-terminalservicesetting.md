---
title: Méthode SetPrimaryLicenseServer de la classe Win32_TerminalServiceSetting
description: Définit le serveur de licences donné comme première entrée de la liste des serveurs de licences spécifiés.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetPrimaryLicenseServer
- Services Bureau à distance de la méthode SetPrimaryLicenseServer, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetPrimaryLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843253"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="31e83-106">Méthode SetPrimaryLicenseServer de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="31e83-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="31e83-107">Définit le serveur de licences donné comme première entrée de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="31e83-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e83-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31e83-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="31e83-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31e83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31e83-110">*LicenseServerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31e83-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31e83-111">Nom du serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="31e83-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31e83-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31e83-112">Return value</span></span>

<span data-ttu-id="31e83-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="31e83-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="31e83-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="31e83-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e83-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31e83-115">Requirements</span></span>



| <span data-ttu-id="31e83-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31e83-116">Requirement</span></span> | <span data-ttu-id="31e83-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="31e83-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31e83-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31e83-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e83-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="31e83-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31e83-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="31e83-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="31e83-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="31e83-122">Namespace</span></span><br/>                | <span data-ttu-id="31e83-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="31e83-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="31e83-124">MOF</span><span class="sxs-lookup"><span data-stu-id="31e83-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31e83-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31e83-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="31e83-126">DLL</span><span class="sxs-lookup"><span data-stu-id="31e83-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31e83-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31e83-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e83-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31e83-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e83-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="31e83-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





