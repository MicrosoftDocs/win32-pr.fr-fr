---
description: Représente les paramètres pour le service de métrique. Les propriétés de cette classe ne peuvent pas être modifiées directement. Le client doit appeler la méthode ModifyServiceSettings pour modifier l’une de ces propriétés.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Classe Msvm_MetricServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529761"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="ef3e9-105">MSVM \_ MetricServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="ef3e9-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="ef3e9-106">Représente les paramètres pour le service de métrique.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="ef3e9-107">Les propriétés de cette classe ne peuvent pas être modifiées directement.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="ef3e9-108">Le client doit appeler la méthode [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) pour modifier l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="ef3e9-109">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef3e9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef3e9-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="ef3e9-111">Membres</span><span class="sxs-lookup"><span data-stu-id="ef3e9-111">Members</span></span>

<span data-ttu-id="ef3e9-112">La classe **MSVM \_ MetricServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ef3e9-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ef3e9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef3e9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef3e9-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ef3e9-114">Properties</span></span>

<span data-ttu-id="ef3e9-115">La classe **MSVM \_ MetricServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef3e9-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef3e9-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef3e9-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef3e9-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef3e9-119">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-119">A short description of the object.</span></span> <span data-ttu-id="ef3e9-120">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du service métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="ef3e9-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ef3e9-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef3e9-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef3e9-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef3e9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef3e9-124">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ef3e9-124">A description of the object.</span></span> <span data-ttu-id="ef3e9-125">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et elle est toujours définie sur « définit les paramètres du service métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="ef3e9-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ef3e9-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef3e9-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef3e9-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef3e9-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef3e9-129">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-129">A display name for the object.</span></span> <span data-ttu-id="ef3e9-130">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du service métrique Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="ef3e9-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ef3e9-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef3e9-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef3e9-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef3e9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef3e9-134">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ef3e9-135">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ef3e9-136">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef3e9-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ef3e9-137">**MetricsFlushInterval**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef3e9-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef3e9-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ef3e9-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef3e9-140">Définit l’intervalle auquel les mesures doivent être vidées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="ef3e9-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef3e9-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef3e9-141">Requirements</span></span>



| <span data-ttu-id="ef3e9-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef3e9-142">Requirement</span></span> | <span data-ttu-id="ef3e9-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef3e9-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef3e9-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef3e9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ef3e9-145">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef3e9-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef3e9-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef3e9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ef3e9-147">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef3e9-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef3e9-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ef3e9-148">Namespace</span></span><br/>                | <span data-ttu-id="ef3e9-149">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef3e9-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef3e9-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ef3e9-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef3e9-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef3e9-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef3e9-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ef3e9-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef3e9-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef3e9-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef3e9-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef3e9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef3e9-155">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="ef3e9-156">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="ef3e9-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

