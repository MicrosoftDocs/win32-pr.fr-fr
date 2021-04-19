---
title: Méthode InitialProgram de la classe Win32_TSEnvironmentSetting
description: La méthode InitialProgram définit les propriétés du programme de démarrage, telles que le nom, le répertoire de travail et le chemin d’accès du programme à démarrer immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InitialProgram
- Services Bureau à distance de la méthode InitialProgram, classe Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance, méthode InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527568"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="0b482-106">Méthode InitialProgram de la \_ classe Win32 TSEnvironmentSetting</span><span class="sxs-lookup"><span data-stu-id="0b482-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="0b482-107">La méthode **InitialProgram** définit les propriétés du programme de démarrage, telles que le nom, le répertoire de travail et le chemin d’accès du programme à démarrer immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="0b482-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b482-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b482-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="0b482-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b482-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b482-110">*InitialProgramPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b482-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b482-111">Nom et chemin d’accès du programme de démarrage.</span><span class="sxs-lookup"><span data-stu-id="0b482-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="0b482-112">*Démarrer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b482-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b482-113">Chemin d’accès au répertoire de travail du programme de démarrage.</span><span class="sxs-lookup"><span data-stu-id="0b482-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b482-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b482-114">Return value</span></span>

<span data-ttu-id="0b482-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="0b482-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0b482-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0b482-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0b482-117">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="0b482-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b482-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0b482-118">Remarks</span></span>

<span data-ttu-id="0b482-119">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0b482-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0b482-120">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0b482-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0b482-121">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0b482-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0b482-122">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0b482-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b482-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b482-123">Requirements</span></span>



| <span data-ttu-id="0b482-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b482-124">Requirement</span></span> | <span data-ttu-id="0b482-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b482-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b482-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b482-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b482-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b482-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b482-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b482-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b482-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b482-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b482-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b482-130">Namespace</span></span><br/>                | <span data-ttu-id="0b482-131">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="0b482-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0b482-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0b482-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b482-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b482-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b482-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0b482-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b482-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b482-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b482-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b482-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b482-137">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0b482-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

