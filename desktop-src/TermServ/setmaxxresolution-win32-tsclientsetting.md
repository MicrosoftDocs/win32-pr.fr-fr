---
title: Méthode SetMaxXResolution de la classe Win32_TSClientSetting
description: Définit la propriété MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxXResolution
- Services Bureau à distance de la méthode SetMaxXResolution, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ab911fd66c7cf6b4f657d8f9e060eccee80675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465106"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="c2426-106">Méthode SetMaxXResolution de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="c2426-106">SetMaxXResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="c2426-107">Définit la propriété **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="c2426-107">Sets the **MaxXResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2426-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2426-108">Syntax</span></span>


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a><span data-ttu-id="c2426-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2426-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2426-110">*MaxXResolution* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c2426-110">*MaxXResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2426-111">Nouvelle résolution X maximale prise en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="c2426-111">The new maximum X resolution supported by the server.</span></span> <span data-ttu-id="c2426-112">La valeur minimale est 200 et la valeur maximale est 4096.</span><span class="sxs-lookup"><span data-stu-id="c2426-112">The minimum value is 200 and maximum value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2426-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2426-113">Return value</span></span>

<span data-ttu-id="c2426-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="c2426-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c2426-115">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c2426-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="c2426-116">La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="c2426-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2426-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2426-117">Requirements</span></span>



| <span data-ttu-id="c2426-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2426-118">Requirement</span></span> | <span data-ttu-id="c2426-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2426-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2426-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2426-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2426-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2426-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c2426-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2426-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2426-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2426-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c2426-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c2426-124">Namespace</span></span><br/>                | <span data-ttu-id="c2426-125">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c2426-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c2426-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c2426-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2426-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2426-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2426-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c2426-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2426-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2426-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2426-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2426-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2426-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c2426-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





