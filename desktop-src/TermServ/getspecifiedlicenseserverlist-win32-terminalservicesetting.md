---
title: Méthode GetSpecifiedLicenseServerList de la classe Win32_TerminalServiceSetting
description: Récupère la liste des serveurs de licences spécifiés.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetSpecifiedLicenseServerList
- Services Bureau à distance de la méthode GetSpecifiedLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384048"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="04b0d-106">Méthode GetSpecifiedLicenseServerList de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="04b0d-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="04b0d-107">Récupère la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="04b0d-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b0d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04b0d-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="04b0d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04b0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b0d-110">*SpecifiedLSList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04b0d-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04b0d-111">Tableau de chaînes qui reçoit la liste des serveurs de licences.</span><span class="sxs-lookup"><span data-stu-id="04b0d-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="04b0d-112">S’il n’y a aucun serveur de licences, ce groupe est vide.</span><span class="sxs-lookup"><span data-stu-id="04b0d-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b0d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04b0d-113">Return value</span></span>

<span data-ttu-id="04b0d-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="04b0d-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="04b0d-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="04b0d-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b0d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04b0d-116">Requirements</span></span>



| <span data-ttu-id="04b0d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04b0d-117">Requirement</span></span> | <span data-ttu-id="04b0d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="04b0d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b0d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04b0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04b0d-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04b0d-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="04b0d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04b0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04b0d-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04b0d-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="04b0d-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04b0d-123">Namespace</span></span><br/>                | <span data-ttu-id="04b0d-124">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="04b0d-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="04b0d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="04b0d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04b0d-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04b0d-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="04b0d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="04b0d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b0d-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b0d-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b0d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04b0d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b0d-130">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="04b0d-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="04b0d-131">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="04b0d-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="04b0d-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="04b0d-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="04b0d-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="04b0d-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="04b0d-134">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="04b0d-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





