---
description: La \_ classe d’association CIM DeviceConnection représente au moins deux appareils connectés.
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: CIM_DeviceConnection, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201032"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a><span data-ttu-id="4763f-103">CIM_DeviceConnection, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4763f-103">CIM_DeviceConnection class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4763f-104">La classe d’association **CIM \_ DeviceConnection** représente au moins deux appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="4763f-104">The **CIM\_DeviceConnection** association class represents two or more connected devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4763f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="4763f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4763f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4763f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4763f-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4763f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4763f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4763f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4763f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4763f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a><span data-ttu-id="4763f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4763f-110">Members</span></span>

<span data-ttu-id="4763f-111">La classe **CIM \_ DeviceConnection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4763f-111">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="4763f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4763f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4763f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4763f-113">Properties</span></span>

<span data-ttu-id="4763f-114">La classe **CIM \_ DeviceConnection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4763f-114">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4763f-115">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="4763f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4763f-116">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="4763f-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4763f-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4763f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4763f-118">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4763f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4763f-119">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="4763f-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a logical device.</span></span>

</dd> <dt>

<span data-ttu-id="4763f-120">**Charge**</span><span class="sxs-lookup"><span data-stu-id="4763f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4763f-121">Type de données **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="4763f-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4763f-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4763f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4763f-123">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)</span><span class="sxs-lookup"><span data-stu-id="4763f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4763f-124">[**\_ LogicalDevice CIM**](cim-logicaldevice.md) qui décrit un deuxième périphérique logique connecté à l’appareil antécédent.</span><span class="sxs-lookup"><span data-stu-id="4763f-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes a second logical device connected to the Antecedent device.</span></span>

</dd> <dt>

<span data-ttu-id="4763f-125">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="4763f-125">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4763f-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4763f-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4763f-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4763f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4763f-128">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits »)</span><span class="sxs-lookup"><span data-stu-id="4763f-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4763f-129">Lorsque plusieurs largeurs de données de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="4763f-129">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="4763f-130">La largeur des données est spécifiée en bits.</span><span class="sxs-lookup"><span data-stu-id="4763f-130">Data width is specified in bits.</span></span> <span data-ttu-id="4763f-131">Si la largeur des données n’est pas négociée, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="4763f-131">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="4763f-132">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="4763f-132">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4763f-133">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4763f-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4763f-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4763f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4763f-135">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="4763f-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="4763f-136">Lorsque plusieurs vitesses de bus ou de connexion sont possibles, cette propriété définit celle qui est utilisée entre les appareils.</span><span class="sxs-lookup"><span data-stu-id="4763f-136">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="4763f-137">La vitesse est spécifiée en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="4763f-137">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="4763f-138">Si les vitesses de connexion ou de bus ne sont pas négociées, ou si ces informations ne sont pas disponibles ou importantes pour la gestion des appareils, la propriété doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="4763f-138">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4763f-139">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4763f-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4763f-140">Notes</span><span class="sxs-lookup"><span data-stu-id="4763f-140">Remarks</span></span>

<span data-ttu-id="4763f-141">La classe **CIM \_ DeviceConnection** est dérivée de la [**\_ dépendance CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4763f-141">The **CIM\_DeviceConnection** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="4763f-142">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="4763f-142">WMI does not implement this class.</span></span> <span data-ttu-id="4763f-143">Pour plus d’informations sur les classes dérivées de **CIM \_ DeviceConnection**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4763f-143">For more information about classes derived from **CIM\_DeviceConnection**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4763f-144">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="4763f-144">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4763f-145">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4763f-145">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4763f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4763f-146">Requirements</span></span>



| <span data-ttu-id="4763f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4763f-147">Requirement</span></span> | <span data-ttu-id="4763f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="4763f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4763f-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4763f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4763f-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4763f-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4763f-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4763f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4763f-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4763f-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4763f-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4763f-153">Namespace</span></span><br/>                | <span data-ttu-id="4763f-154">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4763f-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4763f-155">MOF</span><span class="sxs-lookup"><span data-stu-id="4763f-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4763f-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4763f-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4763f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4763f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4763f-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4763f-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4763f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4763f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4763f-160">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="4763f-160">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

