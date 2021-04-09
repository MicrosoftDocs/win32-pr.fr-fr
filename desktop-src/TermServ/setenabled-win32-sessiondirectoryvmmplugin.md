---
title: Méthode SetEnabled de la classe Win32_SessionDirectoryVMMPlugin
description: Active ou désactive le plug-in.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEnabled
- Services Bureau à distance de la méthode SetEnabled, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode SetEnabled
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743612"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="82182-106">Méthode SetEnabled de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="82182-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="82182-107">Active ou désactive le plug-in.</span><span class="sxs-lookup"><span data-stu-id="82182-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="82182-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82182-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="82182-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82182-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82182-110">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82182-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82182-111">Indique si le plug-in est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="82182-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="82182-112">**True** si le plug-in est activé ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="82182-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82182-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82182-113">Return value</span></span>

<span data-ttu-id="82182-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="82182-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="82182-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="82182-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="82182-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82182-116">Requirements</span></span>



| <span data-ttu-id="82182-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82182-117">Requirement</span></span> | <span data-ttu-id="82182-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="82182-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82182-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82182-119">Minimum supported client</span></span><br/> | <span data-ttu-id="82182-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="82182-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="82182-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82182-121">Minimum supported server</span></span><br/> | <span data-ttu-id="82182-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="82182-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="82182-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82182-123">Namespace</span></span><br/>                | <span data-ttu-id="82182-124">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="82182-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="82182-125">MOF</span><span class="sxs-lookup"><span data-stu-id="82182-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82182-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82182-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="82182-127">DLL</span><span class="sxs-lookup"><span data-stu-id="82182-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82182-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82182-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82182-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82182-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82182-130">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="82182-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





