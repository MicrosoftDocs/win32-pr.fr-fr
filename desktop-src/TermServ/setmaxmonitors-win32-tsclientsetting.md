---
title: Méthode SetMaxMonitors de la classe Win32_TSClientSetting
description: Définit la propriété MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxMonitors
- Services Bureau à distance de la méthode SetMaxMonitors, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511573"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="c657e-106">Méthode SetMaxMonitors de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="c657e-106">SetMaxMonitors method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="c657e-107">Définit la propriété **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="c657e-107">Sets the **MaxMonitors** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c657e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c657e-108">Syntax</span></span>


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="c657e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c657e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c657e-110">*MaxMonitors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c657e-110">*MaxMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c657e-111">Spécifie le nouveau nombre maximal de moniteurs pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="c657e-111">Specifies the new maximum number of monitors supported by the server.</span></span> <span data-ttu-id="c657e-112">La valeur minimale est 1 et la valeur maximale est 10.</span><span class="sxs-lookup"><span data-stu-id="c657e-112">The minimum value is 1 and the maximum value is 10.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c657e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c657e-113">Return value</span></span>

<span data-ttu-id="c657e-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="c657e-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c657e-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c657e-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="c657e-116">La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="c657e-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="c657e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c657e-117">Requirements</span></span>



| <span data-ttu-id="c657e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c657e-118">Requirement</span></span> | <span data-ttu-id="c657e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c657e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c657e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c657e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c657e-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c657e-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c657e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c657e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c657e-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c657e-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c657e-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c657e-124">Namespace</span></span><br/>                | <span data-ttu-id="c657e-125">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c657e-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c657e-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c657e-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c657e-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c657e-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c657e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c657e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c657e-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c657e-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c657e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c657e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c657e-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c657e-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





