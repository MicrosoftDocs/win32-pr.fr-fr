---
title: Méthode RegisterVMMPlugin de la classe Win32_SessionDirectoryVMMPlugin
description: Inscrit un nouveau plug-in VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RegisterVMMPlugin
- Services Bureau à distance de la méthode RegisterVMMPlugin, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384279"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="73eb6-106">Méthode RegisterVMMPlugin de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="73eb6-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="73eb6-107">Inscrit un nouveau plug-in VMM.</span><span class="sxs-lookup"><span data-stu-id="73eb6-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="73eb6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73eb6-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="73eb6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73eb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73eb6-110">*sName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73eb6-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73eb6-111">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="73eb6-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="73eb6-112">*sProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73eb6-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73eb6-113">Nom du fournisseur de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="73eb6-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="73eb6-114">*sServiceLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73eb6-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73eb6-115">Emplacement du service que le plug-in doit contacter.</span><span class="sxs-lookup"><span data-stu-id="73eb6-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="73eb6-116">*sClassID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73eb6-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73eb6-117">Identificateur de classe du plug-in.</span><span class="sxs-lookup"><span data-stu-id="73eb6-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="73eb6-118">*Priorité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73eb6-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73eb6-119">Priorité du plug-in.</span><span class="sxs-lookup"><span data-stu-id="73eb6-119">The priority of the plug-in.</span></span> <span data-ttu-id="73eb6-120">Plus la valeur est élevée, plus la priorité du plug-in est élevée.</span><span class="sxs-lookup"><span data-stu-id="73eb6-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="73eb6-121">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73eb6-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73eb6-122">Indique si le plug-in est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="73eb6-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="73eb6-123">**True** si le plug-in est activé ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="73eb6-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73eb6-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73eb6-124">Return value</span></span>

<span data-ttu-id="73eb6-125">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="73eb6-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="73eb6-126">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="73eb6-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="73eb6-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73eb6-127">Requirements</span></span>



| <span data-ttu-id="73eb6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73eb6-128">Requirement</span></span> | <span data-ttu-id="73eb6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="73eb6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73eb6-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73eb6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="73eb6-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="73eb6-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73eb6-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73eb6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="73eb6-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73eb6-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="73eb6-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73eb6-134">Namespace</span></span><br/>                | <span data-ttu-id="73eb6-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="73eb6-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="73eb6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="73eb6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73eb6-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73eb6-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="73eb6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="73eb6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73eb6-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73eb6-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73eb6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73eb6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73eb6-141">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="73eb6-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





