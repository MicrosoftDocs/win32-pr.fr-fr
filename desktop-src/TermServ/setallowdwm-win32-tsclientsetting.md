---
title: Méthode SetAllowDwm de la classe Win32_TSClientSetting
description: Définit la propriété AllowDwm.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetAllowDwm
- Services Bureau à distance de la méthode SetAllowDwm, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetAllowDwm
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511759"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="4fdfb-106">Méthode SetAllowDwm de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="4fdfb-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="4fdfb-107">Définit la propriété **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="4fdfb-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fdfb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fdfb-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="4fdfb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fdfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fdfb-110">*AllowDwm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4fdfb-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fdfb-111">Nouvelle valeur de la propriété **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="4fdfb-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fdfb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4fdfb-112">Return value</span></span>

<span data-ttu-id="4fdfb-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="4fdfb-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4fdfb-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4fdfb-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4fdfb-115">La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="4fdfb-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fdfb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fdfb-116">Requirements</span></span>



| <span data-ttu-id="4fdfb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fdfb-117">Requirement</span></span> | <span data-ttu-id="4fdfb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fdfb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fdfb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fdfb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4fdfb-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fdfb-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4fdfb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fdfb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4fdfb-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fdfb-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4fdfb-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4fdfb-123">End of client support</span></span><br/>    | <span data-ttu-id="4fdfb-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fdfb-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4fdfb-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4fdfb-125">End of server support</span></span><br/>    | <span data-ttu-id="4fdfb-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fdfb-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="4fdfb-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4fdfb-127">Namespace</span></span><br/>                | <span data-ttu-id="4fdfb-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="4fdfb-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4fdfb-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4fdfb-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fdfb-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fdfb-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fdfb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4fdfb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fdfb-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fdfb-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fdfb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fdfb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fdfb-134">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4fdfb-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





