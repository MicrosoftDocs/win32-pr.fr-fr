---
title: Méthode SetMaxYResolution de la classe Win32_TSClientSetting
description: Définit la propriété MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxYResolution
- Services Bureau à distance de la méthode SetMaxYResolution, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509923"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="faadd-106">Méthode SetMaxYResolution de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="faadd-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="faadd-107">Définit la propriété **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="faadd-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="faadd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faadd-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="faadd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faadd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faadd-110">*MaxYResolution* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="faadd-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faadd-111">Nouvelle résolution Y maximale prise en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="faadd-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="faadd-112">La valeur minimale est 200 et la valeur maximale est 2048.</span><span class="sxs-lookup"><span data-stu-id="faadd-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faadd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faadd-113">Return value</span></span>

<span data-ttu-id="faadd-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="faadd-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="faadd-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="faadd-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="faadd-116">La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="faadd-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="faadd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faadd-117">Requirements</span></span>



| <span data-ttu-id="faadd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faadd-118">Requirement</span></span> | <span data-ttu-id="faadd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="faadd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="faadd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faadd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="faadd-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="faadd-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="faadd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faadd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="faadd-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="faadd-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="faadd-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="faadd-124">Namespace</span></span><br/>                | <span data-ttu-id="faadd-125">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="faadd-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="faadd-126">MOF</span><span class="sxs-lookup"><span data-stu-id="faadd-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faadd-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faadd-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="faadd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="faadd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faadd-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faadd-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faadd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faadd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faadd-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="faadd-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





