---
title: Méthode GetTSLanaIds de la classe Win32_TerminalServiceSetting
description: Obtient les ID de carte réseau local NetBIOS (LANA) et les descriptions des cartes réseau Services Bureau à distance.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetTSLanaIds
- Services Bureau à distance de la méthode GetTSLanaIds, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467035"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="cc5f0-106">Méthode GetTSLanaIds de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="cc5f0-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="cc5f0-107">La méthode **GetTSLanaIds** obtient les ID de carte réseau locale NetBIOS et les descriptions des cartes réseau services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cc5f0-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5f0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc5f0-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="cc5f0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc5f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc5f0-110">*LanaIdList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc5f0-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5f0-111">Tableau de numéros LANA.</span><span class="sxs-lookup"><span data-stu-id="cc5f0-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="cc5f0-112">*LanaIdDescriptions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc5f0-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5f0-113">Tableau de descriptions de LANA correspondant au tableau *LanaIdList* .</span><span class="sxs-lookup"><span data-stu-id="cc5f0-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc5f0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc5f0-114">Return value</span></span>

<span data-ttu-id="cc5f0-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="cc5f0-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cc5f0-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cc5f0-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc5f0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cc5f0-117">Remarks</span></span>

<span data-ttu-id="cc5f0-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="cc5f0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cc5f0-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cc5f0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cc5f0-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="cc5f0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cc5f0-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cc5f0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc5f0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc5f0-122">Requirements</span></span>



| <span data-ttu-id="cc5f0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc5f0-123">Requirement</span></span> | <span data-ttu-id="cc5f0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc5f0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5f0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc5f0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cc5f0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc5f0-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc5f0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc5f0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cc5f0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc5f0-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc5f0-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cc5f0-129">Namespace</span></span><br/>                | <span data-ttu-id="cc5f0-130">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="cc5f0-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cc5f0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cc5f0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc5f0-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc5f0-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc5f0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cc5f0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc5f0-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc5f0-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc5f0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc5f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc5f0-136">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cc5f0-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

