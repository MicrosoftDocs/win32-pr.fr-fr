---
description: Ajoute des paramètres de DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) à un port de Fibre Channel synthétique sur une machine virtuelle.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Méthode AddFibreChannelChap de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952054"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1b383-103">Méthode AddFibreChannelChap de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="1b383-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1b383-104">Ajoute des paramètres de DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) à un port de Fibre Channel synthétique sur une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1b383-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="1b383-105">Cette méthode échoue si l’ordinateur virtuel est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1b383-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b383-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b383-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="1b383-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b383-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b383-108">*FcPortSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b383-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b383-109">Tableau de chaînes qui contient une instance incorporée de la classe [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) qui décrit les paramètres des ports de Fibre Channel synthétique pour les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="1b383-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="1b383-110">La propriété **InstanceID** de chacune de ces instances identifie les éléments à modifier.</span><span class="sxs-lookup"><span data-stu-id="1b383-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="1b383-111">*SecretEncoding* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b383-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b383-112">Spécifie le type d’encodage pour le secret partagé.</span><span class="sxs-lookup"><span data-stu-id="1b383-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="1b383-113">**ASCII imprimable** (1)</span><span class="sxs-lookup"><span data-stu-id="1b383-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="1b383-114">**Binaire** (2)</span><span class="sxs-lookup"><span data-stu-id="1b383-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1b383-115">Sous-son  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b383-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b383-116">Spécifie le secret partagé.</span><span class="sxs-lookup"><span data-stu-id="1b383-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b383-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b383-117">Return value</span></span>

<span data-ttu-id="1b383-118">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b383-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1b383-119">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1b383-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="1b383-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="1b383-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="1b383-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="1b383-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="1b383-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="1b383-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="1b383-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="1b383-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="1b383-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="1b383-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1b383-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="1b383-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1b383-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b383-131">Requirements</span></span>



| <span data-ttu-id="1b383-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b383-132">Requirement</span></span> | <span data-ttu-id="1b383-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b383-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b383-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b383-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1b383-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b383-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1b383-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b383-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1b383-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b383-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1b383-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1b383-138">Namespace</span></span><br/>                | <span data-ttu-id="1b383-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="1b383-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1b383-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1b383-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b383-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b383-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b383-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1b383-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b383-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1b383-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1b383-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b383-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b383-145">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="1b383-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




