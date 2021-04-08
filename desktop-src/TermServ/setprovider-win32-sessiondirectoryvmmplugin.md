---
title: Méthode SetProvider de la classe Win32_SessionDirectoryVMMPlugin
description: Définit le nom du fournisseur de plug-ins.
ms.assetid: fefb7c19-2bab-4ae3-b88b-20da5fd19ff3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetProvider
- Services Bureau à distance de la méthode SetProvider, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode SetProvider
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetProvider
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205a88ecbd67dcf3b009577fa7384e074cc68487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741477"
---
# <a name="setprovider-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="e7cb6-106">Méthode SetProvider de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="e7cb6-106">SetProvider method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="e7cb6-107">Définit le nom du fournisseur de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-107">Sets the name of the plug-in provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cb6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7cb6-108">Syntax</span></span>


```mof
uint32 SetProvider(
  [in] string sProvider
);
```



## <a name="parameters"></a><span data-ttu-id="e7cb6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7cb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7cb6-110">*sProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7cb6-110">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7cb6-111">Nom du fournisseur de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-111">The name of the plug-in provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7cb6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7cb6-112">Return value</span></span>

<span data-ttu-id="e7cb6-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="e7cb6-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e7cb6-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e7cb6-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7cb6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7cb6-115">Requirements</span></span>



| <span data-ttu-id="e7cb6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7cb6-116">Requirement</span></span> | <span data-ttu-id="e7cb6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7cb6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cb6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7cb6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e7cb6-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7cb6-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e7cb6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7cb6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e7cb6-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7cb6-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e7cb6-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7cb6-122">Namespace</span></span><br/>                | <span data-ttu-id="e7cb6-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e7cb6-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="e7cb6-124">MOF</span><span class="sxs-lookup"><span data-stu-id="e7cb6-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7cb6-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7cb6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e7cb6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7cb6-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7cb6-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7cb6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7cb6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7cb6-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="e7cb6-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





