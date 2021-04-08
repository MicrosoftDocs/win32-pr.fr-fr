---
title: Méthode SetClientWallPaper de la classe Win32_TSEnvironmentSetting
description: La méthode SetClientWallPaper définit la propriété ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetClientWallPaper
- Services Bureau à distance de la méthode SetClientWallPaper, classe Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance, méthode SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741260"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="01afc-106">Méthode SetClientWallPaper de la \_ classe Win32 TSEnvironmentSetting</span><span class="sxs-lookup"><span data-stu-id="01afc-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="01afc-107">La méthode **SetClientWallPaper** définit la propriété **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="01afc-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="01afc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01afc-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="01afc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01afc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01afc-110">*ClientWallPaper* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="01afc-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01afc-111">Indicateur de désactivation ou d’activation de la propriété **ClientWallPaper** , qui spécifie si l’image d’arrière-plan (ou de papier peint) est affichée sur le client.</span><span class="sxs-lookup"><span data-stu-id="01afc-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="01afc-112"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="01afc-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="01afc-113">L’image d’arrière-plan (ou de papier peint) n’est pas affichée sur le client.</span><span class="sxs-lookup"><span data-stu-id="01afc-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="01afc-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="01afc-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="01afc-115">L’image d’arrière-plan (ou de papier peint) est affichée sur le client.</span><span class="sxs-lookup"><span data-stu-id="01afc-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01afc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01afc-116">Return value</span></span>

<span data-ttu-id="01afc-117">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="01afc-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="01afc-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="01afc-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="01afc-119">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="01afc-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="01afc-120">Notes</span><span class="sxs-lookup"><span data-stu-id="01afc-120">Remarks</span></span>

<span data-ttu-id="01afc-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="01afc-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="01afc-122">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="01afc-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="01afc-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="01afc-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="01afc-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="01afc-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="01afc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01afc-125">Requirements</span></span>



| <span data-ttu-id="01afc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01afc-126">Requirement</span></span> | <span data-ttu-id="01afc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="01afc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01afc-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01afc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="01afc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01afc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01afc-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01afc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="01afc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01afc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01afc-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="01afc-132">Namespace</span></span><br/>                | <span data-ttu-id="01afc-133">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="01afc-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="01afc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="01afc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01afc-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01afc-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="01afc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="01afc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01afc-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01afc-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01afc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01afc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01afc-139">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="01afc-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

