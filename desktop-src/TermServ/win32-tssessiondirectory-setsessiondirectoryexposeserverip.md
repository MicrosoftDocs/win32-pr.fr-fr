---
title: Méthode SetSessionDirectoryExposeServerIP de la classe Win32_TSSessionDirectory
description: Définit la propriété SessionDirectoryExposeServerIP.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionDirectoryExposeServerIP
- Services Bureau à distance de la méthode SetSessionDirectoryExposeServerIP, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetSessionDirectoryExposeServerIP
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941982"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="96b11-106">Méthode SetSessionDirectoryExposeServerIP de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="96b11-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="96b11-107">Définit la propriété **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="96b11-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96b11-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="96b11-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96b11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b11-110">*SessionDirectoryExposeServerIP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96b11-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b11-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96b11-111">Type: **uint32**</span></span>

<span data-ttu-id="96b11-112">Indicateur de désactivation ou d’activation de la propriété **SessionDirectoryExposeServerIP** qui autorise ou refuse la récupération de l’adresse IP de l’annuaire de sessions.</span><span class="sxs-lookup"><span data-stu-id="96b11-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="96b11-113"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="96b11-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="96b11-114">Désactivez la propriété.</span><span class="sxs-lookup"><span data-stu-id="96b11-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="96b11-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="96b11-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="96b11-116">Activez la propriété.</span><span class="sxs-lookup"><span data-stu-id="96b11-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b11-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96b11-117">Return value</span></span>

<span data-ttu-id="96b11-118">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96b11-118">Type: **uint32**</span></span>

<span data-ttu-id="96b11-119">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="96b11-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="96b11-120">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="96b11-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="96b11-121">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="96b11-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="96b11-122">Notes</span><span class="sxs-lookup"><span data-stu-id="96b11-122">Remarks</span></span>

<span data-ttu-id="96b11-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="96b11-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="96b11-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="96b11-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="96b11-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="96b11-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="96b11-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="96b11-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="96b11-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96b11-127">Requirements</span></span>



| <span data-ttu-id="96b11-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96b11-128">Requirement</span></span> | <span data-ttu-id="96b11-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="96b11-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96b11-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96b11-130">Minimum supported client</span></span><br/> | <span data-ttu-id="96b11-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="96b11-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="96b11-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96b11-132">Minimum supported server</span></span><br/> | <span data-ttu-id="96b11-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96b11-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96b11-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="96b11-134">Namespace</span></span><br/>                | <span data-ttu-id="96b11-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="96b11-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="96b11-136">MOF</span><span class="sxs-lookup"><span data-stu-id="96b11-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96b11-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96b11-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="96b11-138">DLL</span><span class="sxs-lookup"><span data-stu-id="96b11-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96b11-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96b11-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b11-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96b11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b11-141">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="96b11-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

