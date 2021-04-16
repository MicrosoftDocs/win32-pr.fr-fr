---
title: Méthode SetHomeDirectory de la classe Win32_TerminalServiceSetting
description: Définit la propriété TerminalServicesHomeDirectory de la classe.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetHomeDirectory
- Services Bureau à distance de la méthode SetHomeDirectory, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508509"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d3537-106">Méthode SetHomeDirectory de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="d3537-106">SetHomeDirectory method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d3537-107">La méthode **SetHomeDirectory** définit la propriété **TerminalServicesHomeDirectory** de la classe.</span><span class="sxs-lookup"><span data-stu-id="d3537-107">The **SetHomeDirectory** method sets the **TerminalServicesHomeDirectory** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3537-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3537-108">Syntax</span></span>


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="d3537-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3537-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3537-110">*HomeDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3537-110">*HomeDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3537-111">Nouvelle valeur de la propriété **TerminalServicesHomeDirectory** , qui spécifie le répertoire racine de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d3537-111">The new value for the **TerminalServicesHomeDirectory** property, which specifies the computer's root directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3537-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3537-112">Return value</span></span>

<span data-ttu-id="d3537-113">Retourne une réussite en cas de réussite ; Sinon, retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="d3537-113">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="d3537-114">Pour obtenir la liste des codes d’erreur WMI, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d3537-114">For a list of WMI error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3537-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d3537-115">Remarks</span></span>

<span data-ttu-id="d3537-116">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3537-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3537-117">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d3537-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d3537-118">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d3537-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3537-119">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d3537-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3537-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3537-120">Requirements</span></span>



| <span data-ttu-id="d3537-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3537-121">Requirement</span></span> | <span data-ttu-id="d3537-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3537-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3537-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3537-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d3537-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3537-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3537-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3537-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d3537-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3537-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3537-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3537-127">Namespace</span></span><br/>                | <span data-ttu-id="d3537-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d3537-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d3537-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d3537-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3537-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3537-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3537-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d3537-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3537-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3537-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3537-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3537-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3537-134">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d3537-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

