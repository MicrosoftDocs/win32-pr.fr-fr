---
description: Définit les paramètres de migration du système virtuel qui est géré par une instance de la \_ classe CIM VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Classe CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756273"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="3a763-103">\_Classe CIM VirtualSystemMigrationSettingData</span><span class="sxs-lookup"><span data-stu-id="3a763-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="3a763-104">Définit les paramètres de migration du système virtuel qui est géré par une instance de la classe [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a763-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a763-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a763-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="3a763-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3a763-106">Members</span></span>

<span data-ttu-id="3a763-107">La classe **CIM \_ VirtualSystemMigrationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a763-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3a763-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a763-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a763-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3a763-109">Properties</span></span>

<span data-ttu-id="3a763-110">La classe **CIM \_ VirtualSystemMigrationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a763-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a763-111">**Bande passante**</span><span class="sxs-lookup"><span data-stu-id="3a763-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a763-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a763-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a763-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a763-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a763-114">Qualificateurs : [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span><span class="sxs-lookup"><span data-stu-id="3a763-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="3a763-115">Bande passante affectée à une opération de migration de système virtuel ou demandée pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="3a763-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="3a763-116">« 0 » est la bande passante par défaut pour les demandes de migration.</span><span class="sxs-lookup"><span data-stu-id="3a763-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="3a763-117">Les propriétés de la **bande passante** et de la **priorité** peuvent être utilisées conjointement.</span><span class="sxs-lookup"><span data-stu-id="3a763-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="3a763-118">Les processus de migration ayant les valeurs de **priorité** les plus élevées partagent la bande passante disponible en fonction de la bande passante demandée.</span><span class="sxs-lookup"><span data-stu-id="3a763-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="3a763-119">Si la bande passante n’est pas consommée par cet ensemble de processus, les processus de migration avec les valeurs de **priorité** inférieure égale suivantes partagent la bande passante restante.</span><span class="sxs-lookup"><span data-stu-id="3a763-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="3a763-120">Si davantage de bande passante subsistent, les processus de migration avec les valeurs de **priorité** inférieure égale suivante sont pris en compte.</span><span class="sxs-lookup"><span data-stu-id="3a763-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="3a763-121">L’unité utilisée dans la propriété **Bandwidth** est spécifiée par la valeur de la propriété **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="3a763-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="3a763-122">Si la valeur de la propriété **BandwidthUnit** est « percent », les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="3a763-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="3a763-123">La valeur de la propriété de **bande passante** doit être comprise entre « 0 » et « 100 », avec des valeurs supérieures indiquant une bande passante plus élevée.</span><span class="sxs-lookup"><span data-stu-id="3a763-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="3a763-124">La valeur « 100 » indique toute la bande passante disponible pour effectuer les opérations de migration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="3a763-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="3a763-125">Les valeurs comprises entre « 1 » et « 100 » sont corrélées de façon linéaire avec la plage de bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="3a763-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="3a763-126">Par exemple, la valeur 50 demande la moitié de la bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="3a763-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="3a763-127">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="3a763-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a763-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a763-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a763-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a763-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a763-130">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Bande passante**»), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="3a763-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="3a763-131">Unité utilisée par la propriété de **bande passante** .</span><span class="sxs-lookup"><span data-stu-id="3a763-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="3a763-132">La valeur de cette propriété doit être une valeur légale du qualificateur d’unités de programmation défini dans l’annexe C. 1 de DSP0004 V 2.4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3a763-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="3a763-133">Les profils tels que DMTF DSP1081 définissent la façon dont les clients peuvent découvrir l’ensemble d’unités pris en charge par une implémentation, ainsi que les plages et les incréments pour les valeurs de la propriété **Bandwidth** .</span><span class="sxs-lookup"><span data-stu-id="3a763-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="3a763-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="3a763-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a763-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a763-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a763-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a763-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a763-137">Type d’opération de migration à effectuer.</span><span class="sxs-lookup"><span data-stu-id="3a763-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a763-138">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3a763-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a763-139">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="3a763-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="3a763-140">En **direct** (2)</span><span class="sxs-lookup"><span data-stu-id="3a763-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="3a763-141">**Reprendre** (3)</span><span class="sxs-lookup"><span data-stu-id="3a763-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="3a763-142">**Redémarrer** (4)</span><span class="sxs-lookup"><span data-stu-id="3a763-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a763-143">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="3a763-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a763-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a763-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a763-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a763-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a763-146">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")</span><span class="sxs-lookup"><span data-stu-id="3a763-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="3a763-147">Type de transport à appliquer si la valeur de **TransportType** est « 1 » (autre).</span><span class="sxs-lookup"><span data-stu-id="3a763-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="3a763-148">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="3a763-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a763-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a763-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a763-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a763-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a763-151">L’importance de la migration relative que l’implémentation de la migration du système virtuel peut utiliser pour ordonner ou attribuer une préférence entre plusieurs demandes de migration en attente.</span><span class="sxs-lookup"><span data-stu-id="3a763-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="3a763-152">Plus la valeur est faible, plus la priorité est élevée.</span><span class="sxs-lookup"><span data-stu-id="3a763-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="3a763-153">« 0 » est la bande passante par défaut pour les demandes de migration.</span><span class="sxs-lookup"><span data-stu-id="3a763-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="3a763-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="3a763-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a763-155">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a763-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a763-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a763-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a763-157">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")</span><span class="sxs-lookup"><span data-stu-id="3a763-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="3a763-158">Type de transport à appliquer à une opération de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="3a763-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a763-159">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="3a763-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a763-160">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="3a763-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="3a763-161">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="3a763-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="3a763-162">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="3a763-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="3a763-163">**TLS strict** (4)</span><span class="sxs-lookup"><span data-stu-id="3a763-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="3a763-164">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="3a763-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="3a763-165">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="3a763-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a763-166">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="3a763-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a763-167">**Fournisseur réservé** (32768...)</span><span class="sxs-lookup"><span data-stu-id="3a763-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="3a763-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3a763-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3a763-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a763-169">Requirements</span></span>



| <span data-ttu-id="3a763-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a763-170">Requirement</span></span> | <span data-ttu-id="3a763-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a763-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a763-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a763-172">Minimum supported client</span></span><br/> | <span data-ttu-id="3a763-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a763-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3a763-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a763-174">Minimum supported server</span></span><br/> | <span data-ttu-id="3a763-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a763-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3a763-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3a763-176">Namespace</span></span><br/>                | <span data-ttu-id="3a763-177">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3a763-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a763-178">MOF</span><span class="sxs-lookup"><span data-stu-id="3a763-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a763-179"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a763-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a763-180">DLL</span><span class="sxs-lookup"><span data-stu-id="3a763-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a763-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a763-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a763-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a763-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a763-183">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3a763-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

