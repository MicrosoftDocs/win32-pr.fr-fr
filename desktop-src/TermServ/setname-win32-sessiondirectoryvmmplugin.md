---
title: Méthode SetName de la classe Win32_SessionDirectoryVMMPlugin
description: Définit le nom du plug-in.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetName
- Services Bureau à distance de la méthode SetName, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317242"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="236ee-106">Méthode SetName de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="236ee-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="236ee-107">Définit le nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="236ee-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="236ee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="236ee-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="236ee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="236ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="236ee-110">*sName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="236ee-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="236ee-111">Nom du plug-in.</span><span class="sxs-lookup"><span data-stu-id="236ee-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="236ee-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="236ee-112">Return value</span></span>

<span data-ttu-id="236ee-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="236ee-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="236ee-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="236ee-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="236ee-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="236ee-115">Requirements</span></span>



| <span data-ttu-id="236ee-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="236ee-116">Requirement</span></span> | <span data-ttu-id="236ee-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="236ee-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="236ee-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="236ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="236ee-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="236ee-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="236ee-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="236ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="236ee-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="236ee-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="236ee-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="236ee-122">Namespace</span></span><br/>                | <span data-ttu-id="236ee-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="236ee-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="236ee-124">MOF</span><span class="sxs-lookup"><span data-stu-id="236ee-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="236ee-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="236ee-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="236ee-126">DLL</span><span class="sxs-lookup"><span data-stu-id="236ee-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="236ee-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="236ee-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="236ee-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="236ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="236ee-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="236ee-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





