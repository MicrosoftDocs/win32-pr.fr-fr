---
description: Génère un ensemble de noms WWPN (World World-of-Port).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Méthode GenerateWwpn de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516689"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ef209-103">Méthode GenerateWwpn de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="ef209-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ef209-104">Génère un ensemble de noms WWPN (World World-of-Port).</span><span class="sxs-lookup"><span data-stu-id="ef209-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="ef209-105">Les WWPN sont générés à partir de la plage préconfigurée définie par les propriétés **MinimumWWPNAddress** et **MaximumWWPNAddress** de la classe [**\_ VirtualSystemManagementServiceSettingData MSVM**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ef209-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="ef209-106">Si le nombre valide de WWPN pouvant être générés est inférieur au nombre demandé, les entrées restantes du tableau *GeneratedWwpn* auront l’entrée non valide « 0000000000000000 » et la valeur de retour indiquera la réussite (0).</span><span class="sxs-lookup"><span data-stu-id="ef209-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef209-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef209-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="ef209-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef209-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef209-109">*NumberOfWwpns* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef209-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef209-110">Nombre de WWPN à générer.</span><span class="sxs-lookup"><span data-stu-id="ef209-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="ef209-111">*GeneratedWwpn* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ef209-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef209-112">Tableau de chaînes, chacune contenant un WWPN généré.</span><span class="sxs-lookup"><span data-stu-id="ef209-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="ef209-113">Elle est mise en forme sous forme de chaîne sous la forme « 01:23:45:67:89 : AB : CD : EF ».</span><span class="sxs-lookup"><span data-stu-id="ef209-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef209-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef209-114">Return value</span></span>

<span data-ttu-id="ef209-115">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef209-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ef209-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="ef209-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="ef209-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="ef209-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="ef209-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="ef209-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="ef209-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="ef209-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="ef209-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="ef209-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="ef209-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ef209-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ef209-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="ef209-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ef209-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef209-128">Requirements</span></span>



| <span data-ttu-id="ef209-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef209-129">Requirement</span></span> | <span data-ttu-id="ef209-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef209-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef209-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef209-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ef209-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef209-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef209-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef209-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ef209-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef209-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef209-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef209-135">Namespace</span></span><br/>                | <span data-ttu-id="ef209-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef209-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef209-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ef209-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef209-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef209-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef209-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ef209-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef209-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef209-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef209-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef209-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef209-142">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="ef209-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




