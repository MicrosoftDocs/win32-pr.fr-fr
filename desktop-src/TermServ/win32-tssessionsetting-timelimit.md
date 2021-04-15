---
title: Méthode TimeLimit de la classe Win32_TSSessionSetting
description: Définit la durée maximale allouée au type de limite de session spécifié.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TimeLimit
- Services Bureau à distance de la méthode TimeLimit, classe Win32_TSSessionSetting
- Win32_TSSessionSetting de la classe Services Bureau à distance, méthode TimeLimit
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508321"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="c1da6-106">Méthode TimeLimit de la \_ classe Win32 TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="c1da6-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="c1da6-107">Définit la durée maximale allouée au type de limite de session spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1da6-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1da6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1da6-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="c1da6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1da6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1da6-110">*SessionLimitType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1da6-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1da6-111">Spécifie le type de propriété de limite de session que la méthode définit.</span><span class="sxs-lookup"><span data-stu-id="c1da6-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="c1da6-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="c1da6-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="c1da6-113">La méthode définit la propriété **ActiveSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="c1da6-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="c1da6-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="c1da6-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="c1da6-115">La méthode définit la propriété **DisconnectedSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="c1da6-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="c1da6-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="c1da6-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="c1da6-117">La méthode définit la propriété **IdleSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="c1da6-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1da6-118">*ValueLimit* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1da6-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1da6-119">Nouvelle durée maximale, en millisecondes, pour la propriété spécifiée par le paramètre *SessionLimitType* .</span><span class="sxs-lookup"><span data-stu-id="c1da6-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="c1da6-120">La valeur zéro indique qu’il n’y a aucune limite de session.</span><span class="sxs-lookup"><span data-stu-id="c1da6-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1da6-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1da6-121">Return value</span></span>

<span data-ttu-id="c1da6-122">Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="c1da6-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c1da6-123">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c1da6-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="c1da6-124">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c1da6-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1da6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c1da6-125">Remarks</span></span>

<span data-ttu-id="c1da6-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c1da6-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c1da6-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c1da6-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c1da6-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c1da6-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c1da6-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c1da6-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1da6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1da6-130">Requirements</span></span>



| <span data-ttu-id="c1da6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1da6-131">Requirement</span></span> | <span data-ttu-id="c1da6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1da6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1da6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1da6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c1da6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1da6-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1da6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1da6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c1da6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1da6-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1da6-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1da6-137">Namespace</span></span><br/>                | <span data-ttu-id="c1da6-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="c1da6-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c1da6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c1da6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1da6-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1da6-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1da6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c1da6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1da6-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1da6-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1da6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1da6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1da6-144">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c1da6-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

