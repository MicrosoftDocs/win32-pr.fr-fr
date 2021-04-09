---
title: Méthode SetColorDepth de la classe Win32_TSClientSetting
description: La méthode SetColorDepth définit la propriété ColorDepth pour la classe.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetColorDepth
- Services Bureau à distance de la méthode SetColorDepth, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942715"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="b25c1-106">Méthode SetColorDepth de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="b25c1-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="b25c1-107">La méthode **SetColorDepth** définit la propriété **ColorDepth** pour la classe.</span><span class="sxs-lookup"><span data-stu-id="b25c1-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25c1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b25c1-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="b25c1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b25c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b25c1-110">*ColorDepth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b25c1-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b25c1-111">Nouvelle valeur de la propriété **ColorDepth** .</span><span class="sxs-lookup"><span data-stu-id="b25c1-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="b25c1-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b25c1-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b25c1-113">8 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="b25c1-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="b25c1-114"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="b25c1-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="b25c1-115">15 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="b25c1-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="b25c1-116"><span id="3"></span>**1,3**</span><span class="sxs-lookup"><span data-stu-id="b25c1-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="b25c1-117">16 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="b25c1-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="b25c1-118"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="b25c1-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="b25c1-119">24 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="b25c1-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="b25c1-120"><span id="5"></span>**5,5**</span><span class="sxs-lookup"><span data-stu-id="b25c1-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="b25c1-121">32 bits par pixel</span><span class="sxs-lookup"><span data-stu-id="b25c1-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b25c1-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b25c1-122">Return value</span></span>

<span data-ttu-id="b25c1-123">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="b25c1-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b25c1-124">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b25c1-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b25c1-125">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="b25c1-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b25c1-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b25c1-126">Remarks</span></span>

<span data-ttu-id="b25c1-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b25c1-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b25c1-128">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b25c1-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b25c1-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b25c1-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b25c1-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b25c1-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b25c1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b25c1-131">Requirements</span></span>



| <span data-ttu-id="b25c1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b25c1-132">Requirement</span></span> | <span data-ttu-id="b25c1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b25c1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b25c1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b25c1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b25c1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b25c1-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b25c1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b25c1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b25c1-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b25c1-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b25c1-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b25c1-138">Namespace</span></span><br/>                | <span data-ttu-id="b25c1-139">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="b25c1-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b25c1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b25c1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b25c1-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b25c1-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b25c1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b25c1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25c1-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25c1-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b25c1-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b25c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25c1-145">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="b25c1-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

