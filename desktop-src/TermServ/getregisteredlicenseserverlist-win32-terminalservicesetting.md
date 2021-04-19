---
title: Méthode GetRegisteredLicenseServerList de la classe Win32_TerminalServiceSetting
description: Obtient la liste des serveurs de licences inscrits.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetRegisteredLicenseServerList
- Services Bureau à distance de la méthode GetRegisteredLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetRegisteredLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513636"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="66251-106">Méthode GetRegisteredLicenseServerList de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="66251-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="66251-107">Obtient la liste des serveurs de licences inscrits.</span><span class="sxs-lookup"><span data-stu-id="66251-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="66251-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66251-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="66251-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66251-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66251-110">*RegisteredLSList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="66251-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66251-111">Tableau de chaînes qui reçoit la liste des serveurs de licences inscrits.</span><span class="sxs-lookup"><span data-stu-id="66251-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="66251-112">Si aucun serveur de licences n’est inscrit, ce groupe est vide.</span><span class="sxs-lookup"><span data-stu-id="66251-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66251-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66251-113">Return value</span></span>

<span data-ttu-id="66251-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="66251-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="66251-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="66251-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="66251-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66251-116">Requirements</span></span>



| <span data-ttu-id="66251-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66251-117">Requirement</span></span> | <span data-ttu-id="66251-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="66251-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66251-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66251-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66251-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="66251-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="66251-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66251-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66251-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66251-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="66251-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66251-123">Namespace</span></span><br/>                | <span data-ttu-id="66251-124">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="66251-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="66251-125">MOF</span><span class="sxs-lookup"><span data-stu-id="66251-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66251-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66251-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="66251-127">DLL</span><span class="sxs-lookup"><span data-stu-id="66251-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66251-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66251-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66251-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66251-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66251-130">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="66251-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





