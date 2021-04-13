---
title: Méthode SchedulePatch de la classe Win32_RDMSVirtualDesktopCollection
description: Planifie un travail d’approvisionnement des mises à jour logicielles qui installe les mises à jour logicielles sur les machines virtuelles d’une collection de bureaux virtuels.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SchedulePatch
- Services Bureau à distance de la méthode SchedulePatch, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465111"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="f54d5-106">Méthode SchedulePatch de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="f54d5-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="f54d5-107">Planifie un travail d’approvisionnement des mises à jour logicielles qui installe les mises à jour logicielles sur les machines virtuelles d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f54d5-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f54d5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f54d5-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="f54d5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f54d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f54d5-110">*StartTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f54d5-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="f54d5-111">Le système ne déconnecte pas les utilisateurs des ordinateurs virtuels avant l’heure spécifiée dans le paramètre *ForceLogOffTime* .</span><span class="sxs-lookup"><span data-stu-id="f54d5-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="f54d5-112">Date et heure d’installation des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f54d5-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="f54d5-113">*ForceLogOffTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f54d5-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f54d5-114">Date et heure auxquelles le système déconnecte les utilisateurs des ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="f54d5-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="f54d5-115">*JobInputXml* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f54d5-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f54d5-116">Chaîne au format XML qui contient les informations de la tâche de mise à jour logicielle.</span><span class="sxs-lookup"><span data-stu-id="f54d5-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f54d5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f54d5-117">Return value</span></span>

<span data-ttu-id="f54d5-118">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="f54d5-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f54d5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f54d5-119">Requirements</span></span>



| <span data-ttu-id="f54d5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f54d5-120">Requirement</span></span> | <span data-ttu-id="f54d5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f54d5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f54d5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f54d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f54d5-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f54d5-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f54d5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f54d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f54d5-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f54d5-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f54d5-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f54d5-126">Namespace</span></span><br/>                | <span data-ttu-id="f54d5-127">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="f54d5-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f54d5-128">MOF</span><span class="sxs-lookup"><span data-stu-id="f54d5-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f54d5-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f54d5-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f54d5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f54d5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f54d5-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f54d5-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f54d5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f54d5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f54d5-133">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="f54d5-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





