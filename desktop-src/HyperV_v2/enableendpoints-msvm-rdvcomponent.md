---
description: Demande à l’appareil virtuel Services Bureau à distance de démarrer une connexion de canal avec l’ordinateur virtuel.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Méthode EnableEndPoints de la classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201585"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="fbda8-103">Méthode EnableEndPoints de la \_ classe RdvComponent MSVM</span><span class="sxs-lookup"><span data-stu-id="fbda8-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="fbda8-104">Demande à l’appareil virtuel Services Bureau à distance de démarrer une connexion de canal avec l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fbda8-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbda8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbda8-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="fbda8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbda8-106">Parameters</span></span>

<span data-ttu-id="fbda8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fbda8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbda8-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbda8-108">Return value</span></span>

<span data-ttu-id="fbda8-109">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fbda8-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fbda8-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fbda8-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-111">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fbda8-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-112">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="fbda8-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-113">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="fbda8-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-114">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="fbda8-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-115">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="fbda8-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-116">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="fbda8-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-117">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="fbda8-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-118">**Mémoire insuffisante** (32774)</span><span class="sxs-lookup"><span data-stu-id="fbda8-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fbda8-119">**Fichier introuvable** (32775)</span><span class="sxs-lookup"><span data-stu-id="fbda8-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-120">(32776)</span><span class="sxs-lookup"><span data-stu-id="fbda8-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-121">(32777)</span><span class="sxs-lookup"><span data-stu-id="fbda8-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-122">(32778)</span><span class="sxs-lookup"><span data-stu-id="fbda8-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-123">(32779)</span><span class="sxs-lookup"><span data-stu-id="fbda8-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-124">(32780)</span><span class="sxs-lookup"><span data-stu-id="fbda8-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-125">(32781)</span><span class="sxs-lookup"><span data-stu-id="fbda8-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="fbda8-126">(32782)</span><span class="sxs-lookup"><span data-stu-id="fbda8-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fbda8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbda8-127">Requirements</span></span>



| <span data-ttu-id="fbda8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbda8-128">Requirement</span></span> | <span data-ttu-id="fbda8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbda8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbda8-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbda8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fbda8-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbda8-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbda8-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbda8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fbda8-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbda8-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbda8-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbda8-134">Namespace</span></span><br/>                | <span data-ttu-id="fbda8-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fbda8-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbda8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fbda8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbda8-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbda8-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbda8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fbda8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbda8-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbda8-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbda8-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbda8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbda8-141">**MSVM \_ RdvComponent**</span><span class="sxs-lookup"><span data-stu-id="fbda8-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 




