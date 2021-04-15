---
title: Méthode EmptySpecifiedLicenseServerList de la classe Win32_TerminalServiceSetting
description: Supprime tous les serveurs de licences de la liste des serveurs de licences spécifiés.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EmptySpecifiedLicenseServerList
- Services Bureau à distance de la méthode EmptySpecifiedLicenseServerList, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode EmptySpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467043"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="a4e11-106">Méthode EmptySpecifiedLicenseServerList de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="a4e11-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="a4e11-107">Supprime tous les serveurs de licences de la liste des serveurs de licences spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a4e11-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4e11-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="a4e11-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4e11-109">Parameters</span></span>

<span data-ttu-id="a4e11-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a4e11-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4e11-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4e11-111">Return value</span></span>

<span data-ttu-id="a4e11-112">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="a4e11-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a4e11-113">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e11-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e11-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4e11-114">Requirements</span></span>



| <span data-ttu-id="a4e11-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4e11-115">Requirement</span></span> | <span data-ttu-id="a4e11-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4e11-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e11-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4e11-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e11-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4e11-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a4e11-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4e11-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e11-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a4e11-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a4e11-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4e11-121">Namespace</span></span><br/>                | <span data-ttu-id="a4e11-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a4e11-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a4e11-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a4e11-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4e11-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4e11-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4e11-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a4e11-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4e11-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e11-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e11-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4e11-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e11-128">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a4e11-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a4e11-129">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="a4e11-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a4e11-130">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="a4e11-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a4e11-131">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="a4e11-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a4e11-132">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="a4e11-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





