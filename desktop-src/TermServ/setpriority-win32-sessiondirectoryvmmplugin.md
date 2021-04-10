---
title: Méthode SetPriority de la classe Win32_SessionDirectoryVMMPlugin
description: Définit la priorité du plug-in.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority, méthode Services Bureau à distance
- Méthode SetPriority Services Bureau à distance, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode SetPriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942811"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="65593-106">Méthode SetPriority de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="65593-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="65593-107">Définit la priorité du plug-in.</span><span class="sxs-lookup"><span data-stu-id="65593-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="65593-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65593-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="65593-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65593-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65593-110">*Priorité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65593-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65593-111">Priorité du plug-in.</span><span class="sxs-lookup"><span data-stu-id="65593-111">The priority of the plug-in.</span></span> <span data-ttu-id="65593-112">Plus la valeur est élevée, plus la priorité du plug-in est élevée.</span><span class="sxs-lookup"><span data-stu-id="65593-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="65593-113">La priorité est égale à zéro par défaut.</span><span class="sxs-lookup"><span data-stu-id="65593-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65593-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65593-114">Return value</span></span>

<span data-ttu-id="65593-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="65593-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="65593-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="65593-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="65593-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65593-117">Requirements</span></span>



| <span data-ttu-id="65593-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65593-118">Requirement</span></span> | <span data-ttu-id="65593-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="65593-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65593-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65593-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65593-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65593-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65593-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65593-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65593-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65593-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="65593-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65593-124">Namespace</span></span><br/>                | <span data-ttu-id="65593-125">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="65593-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="65593-126">MOF</span><span class="sxs-lookup"><span data-stu-id="65593-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65593-127"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65593-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="65593-128">DLL</span><span class="sxs-lookup"><span data-stu-id="65593-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65593-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65593-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65593-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65593-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65593-131">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="65593-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





