---
title: Méthode SetColorDepthPolicy de la classe Win32_TSClientSetting
description: La méthode SetColorDepthPolicy définit la propriété ColorDepthPolicy de la classe.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetColorDepthPolicy
- Services Bureau à distance de la méthode SetColorDepthPolicy, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384536"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="0e233-106">Méthode SetColorDepthPolicy de la \_ classe Win32 TSClientSetting</span><span class="sxs-lookup"><span data-stu-id="0e233-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="0e233-107">La méthode **SetColorDepthPolicy** définit la propriété **ColorDepthPolicy** de la classe.</span><span class="sxs-lookup"><span data-stu-id="0e233-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e233-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e233-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="0e233-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e233-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e233-110">*ColorDepthPolicy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e233-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e233-111">Indicateur de désactivation ou d’activation de la propriété **SetColorDepthPolicy** , qui spécifie s’il faut remplacer le paramètre de couleur maximal de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e233-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="0e233-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="0e233-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="0e233-113">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="0e233-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="0e233-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="0e233-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="0e233-115">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="0e233-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e233-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e233-116">Return value</span></span>

<span data-ttu-id="0e233-117">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="0e233-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0e233-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0e233-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0e233-119">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0e233-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e233-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0e233-120">Remarks</span></span>

<span data-ttu-id="0e233-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0e233-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e233-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0e233-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0e233-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0e233-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e233-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0e233-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e233-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e233-125">Requirements</span></span>



| <span data-ttu-id="0e233-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e233-126">Requirement</span></span> | <span data-ttu-id="0e233-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e233-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e233-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e233-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e233-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e233-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e233-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e233-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e233-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e233-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e233-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e233-132">Namespace</span></span><br/>                | <span data-ttu-id="0e233-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0e233-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0e233-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0e233-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e233-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e233-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e233-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0e233-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e233-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e233-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e233-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e233-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e233-139">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0e233-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

