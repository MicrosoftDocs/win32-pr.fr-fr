---
description: Représente les paramètres pour le service synthétique 3D présent sur un système hôte unique.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Classe Msvm_Synthetic3DServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114958"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="fe884-103">MSVM \_ Synthetic3DServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="fe884-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="fe884-104">Représente les paramètres pour le service synthétique 3D présent sur un système hôte unique.</span><span class="sxs-lookup"><span data-stu-id="fe884-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="fe884-105">Les propriétés de cette classe ne peuvent pas être modifiées directement.</span><span class="sxs-lookup"><span data-stu-id="fe884-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="fe884-106">Le client doit appeler la méthode [**MSVM \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) pour modifier l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fe884-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="fe884-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fe884-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe884-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe884-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="fe884-109">Membres</span><span class="sxs-lookup"><span data-stu-id="fe884-109">Members</span></span>

<span data-ttu-id="fe884-110">La classe **MSVM \_ Synthetic3DServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fe884-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fe884-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe884-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe884-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fe884-112">Properties</span></span>

<span data-ttu-id="fe884-113">La classe **MSVM \_ Synthetic3DServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fe884-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe884-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fe884-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe884-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fe884-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe884-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe884-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe884-117">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fe884-117">A short description of the object.</span></span> <span data-ttu-id="fe884-118">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fe884-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe884-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe884-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe884-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fe884-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe884-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe884-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe884-122">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="fe884-122">A description of the object.</span></span> <span data-ttu-id="fe884-123">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fe884-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe884-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fe884-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe884-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fe884-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe884-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe884-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe884-127">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fe884-127">A display name for the object.</span></span> <span data-ttu-id="fe884-128">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fe884-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fe884-129">**GPUOvercommitEnabled**</span><span class="sxs-lookup"><span data-stu-id="fe884-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe884-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fe884-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe884-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe884-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe884-132">Contrôle si l’attribution de l’ordinateur virtuel prend en compte les limitations de mémoire du GPU.</span><span class="sxs-lookup"><span data-stu-id="fe884-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="fe884-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe884-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe884-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fe884-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe884-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fe884-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe884-136">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="fe884-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fe884-137">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="fe884-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fe884-138">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fe884-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe884-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe884-139">Requirements</span></span>



| <span data-ttu-id="fe884-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe884-140">Requirement</span></span> | <span data-ttu-id="fe884-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe884-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe884-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe884-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fe884-143">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe884-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fe884-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe884-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fe884-145">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe884-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe884-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fe884-146">Namespace</span></span><br/>                | <span data-ttu-id="fe884-147">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fe884-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe884-148">MOF</span><span class="sxs-lookup"><span data-stu-id="fe884-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe884-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe884-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe884-150">DLL</span><span class="sxs-lookup"><span data-stu-id="fe884-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe884-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe884-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

