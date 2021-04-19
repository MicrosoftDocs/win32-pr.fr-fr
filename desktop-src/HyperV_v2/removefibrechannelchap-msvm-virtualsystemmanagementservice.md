---
description: Supprime les paramètres DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) d’un port de Fibre Channel synthétique dans un ordinateur virtuel.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Méthode RemoveFibreChannelChap de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515273"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a8e27-103">Méthode RemoveFibreChannelChap de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="a8e27-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a8e27-104">Supprime les paramètres DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) d’un port de Fibre Channel synthétique dans un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a8e27-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="a8e27-105">Cette méthode échoue si l’ordinateur virtuel est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a8e27-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e27-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8e27-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="a8e27-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8e27-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e27-108">*FcPortSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8e27-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e27-109">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) qui définit les ports de Fibre Channel synthétiques à partir desquels supprimer les paramètres DH-chap.</span><span class="sxs-lookup"><span data-stu-id="a8e27-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="a8e27-110">La propriété **InstanceID** de chacune de ces instances identifie les éléments à modifier.</span><span class="sxs-lookup"><span data-stu-id="a8e27-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e27-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8e27-111">Return value</span></span>

<span data-ttu-id="a8e27-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8e27-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a8e27-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a8e27-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-114">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="a8e27-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-115">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="a8e27-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-116">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="a8e27-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-117">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="a8e27-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-118">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="a8e27-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-119">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="a8e27-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-120">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="a8e27-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-121">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="a8e27-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-122">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="a8e27-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-123">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a8e27-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a8e27-124">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="a8e27-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a8e27-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8e27-125">Requirements</span></span>



| <span data-ttu-id="a8e27-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8e27-126">Requirement</span></span> | <span data-ttu-id="a8e27-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8e27-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e27-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8e27-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e27-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8e27-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8e27-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8e27-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e27-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8e27-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8e27-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a8e27-132">Namespace</span></span><br/>                | <span data-ttu-id="a8e27-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a8e27-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a8e27-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a8e27-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8e27-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8e27-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8e27-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e27-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e27-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a8e27-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a8e27-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8e27-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e27-139">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a8e27-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




