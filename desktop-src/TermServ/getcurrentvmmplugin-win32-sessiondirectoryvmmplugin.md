---
title: Méthode GetCurrentVMMPlugin de la classe Win32_SessionDirectoryVMMPlugin
description: Obtient le plug-in avec la priorité la plus élevée qui est activé.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetCurrentVMMPlugin
- Services Bureau à distance de la méthode GetCurrentVMMPlugin, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844314"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="e5858-106">Méthode GetCurrentVMMPlugin de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="e5858-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="e5858-107">Obtient le plug-in avec la priorité la plus élevée qui est activé.</span><span class="sxs-lookup"><span data-stu-id="e5858-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5858-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5858-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="e5858-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5858-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5858-110">*sName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5858-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5858-111">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="e5858-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="e5858-112">*sProvider* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5858-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5858-113">Nom du fournisseur de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="e5858-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="e5858-114">*sServiceLocation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5858-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5858-115">Emplacement du service que le plug-in doit contacter.</span><span class="sxs-lookup"><span data-stu-id="e5858-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="e5858-116">*sClassID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5858-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5858-117">Identificateur de classe du plug-in.</span><span class="sxs-lookup"><span data-stu-id="e5858-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="e5858-118">*Priorité* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5858-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5858-119">Priorité du plug-in.</span><span class="sxs-lookup"><span data-stu-id="e5858-119">The priority of the plug-in.</span></span> <span data-ttu-id="e5858-120">Plus la valeur est élevée, plus la priorité du plug-in est élevée.</span><span class="sxs-lookup"><span data-stu-id="e5858-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="e5858-121">*Activé* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5858-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5858-122">Indique si le plug-in est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="e5858-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="e5858-123">**True** si le plug-in est activé ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e5858-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5858-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5858-124">Return value</span></span>

<span data-ttu-id="e5858-125">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e5858-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e5858-126">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e5858-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5858-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5858-127">Requirements</span></span>



| <span data-ttu-id="e5858-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5858-128">Requirement</span></span> | <span data-ttu-id="e5858-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5858-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5858-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5858-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5858-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5858-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e5858-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5858-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5858-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5858-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e5858-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e5858-134">Namespace</span></span><br/>                | <span data-ttu-id="e5858-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e5858-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="e5858-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e5858-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5858-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5858-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5858-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e5858-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5858-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5858-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5858-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5858-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5858-141">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="e5858-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





