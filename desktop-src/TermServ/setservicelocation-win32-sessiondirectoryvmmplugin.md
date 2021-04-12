---
title: Méthode SetServiceLocation de la classe Win32_SessionDirectoryVMMPlugin
description: Définit l’emplacement du service pour le plug-in.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetServiceLocation
- Services Bureau à distance de la méthode SetServiceLocation, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode SetServiceLocation
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508833"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="493b9-106">Méthode SetServiceLocation de la \_ classe Win32 SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="493b9-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="493b9-107">Définit l’emplacement du service pour le plug-in.</span><span class="sxs-lookup"><span data-stu-id="493b9-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="493b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="493b9-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="493b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="493b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="493b9-110">*sServiceLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="493b9-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493b9-111">Emplacement du service que le plug-in doit contacter.</span><span class="sxs-lookup"><span data-stu-id="493b9-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="493b9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="493b9-112">Return value</span></span>

<span data-ttu-id="493b9-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="493b9-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="493b9-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="493b9-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="493b9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="493b9-115">Requirements</span></span>



| <span data-ttu-id="493b9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="493b9-116">Requirement</span></span> | <span data-ttu-id="493b9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="493b9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="493b9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="493b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="493b9-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="493b9-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="493b9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="493b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="493b9-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="493b9-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="493b9-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="493b9-122">Namespace</span></span><br/>                | <span data-ttu-id="493b9-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="493b9-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="493b9-124">MOF</span><span class="sxs-lookup"><span data-stu-id="493b9-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="493b9-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="493b9-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="493b9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="493b9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493b9-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493b9-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493b9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="493b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493b9-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="493b9-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





